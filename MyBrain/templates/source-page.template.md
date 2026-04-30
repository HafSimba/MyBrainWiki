/**
 * Page templates for LLM Wiki
 * Generates frontmatter and content structure for each page type
 */

import type { WikiPageType } from './schema.js';
import { formatDate } from './schema.js';

/**
 * Generate frontmatter for a wiki page
 */
export function generateFrontmatter(
  type: WikiPageType,
  name: string,
  status: 'active' | 'draft' | 'deprecated' = 'active',
  sourceIds: string[] = [],
  tags: string[] = [],
  extra: Record<string, any> = {}
): string {
  const updated = formatDate(new Date());

  let frontmatter = '---\n';
  frontmatter += `type: ${type}\n`;
  frontmatter += `status: ${status}\n`;
  frontmatter += `updated: ${updated}\n`;

  if (sourceIds.length > 0) {
    frontmatter += `source_ids: [${sourceIds.map(id => id.includes(' ') ? `"${id}"` : id).join(', ')}]\n`;
  }

  if (tags.length > 0) {
    frontmatter += `tags: [${tags.join(', ')}]\n`;
  }

  // Add type-specific fields
  if (type === 'source' && extra.source_id) {
    frontmatter += `source_id: ${extra.source_id}\n`;
    frontmatter += `raw_path: ${extra.raw_path || 'raw/sources/' + extra.source_id + '.md'}\n`;
  }

  if (type === 'query' && extra.question) {
    frontmatter += `question: "${extra.question}"\n`;
    frontmatter += `query_date: ${extra.query_date || updated}\n`;
  }

  if (type === 'lint') {
    frontmatter += `coverage: "${extra.coverage || ''}"\n`;
    frontmatter += `orphan_count: ${extra.orphan_count || 0}\n`;
    frontmatter += `contradiction_count: ${extra.contradiction_count || 0}\n`;
  }

  // Add any extra fields
  for (const [key, value] of Object.entries(extra)) {
    if (!['source_id', 'raw_path', 'question', 'query_date', 'coverage', 'orphan_count', 'contradiction_count'].includes(key)) {
      if (typeof value === 'string' && value.includes(' ')) {
        frontmatter += `${key}: "${value}"\n`;
      } else if (Array.isArray(value)) {
        frontmatter += `${key}: [${value.join(', ')}]\n`;
      } else {
        frontmatter += `${key}: ${value}\n`;
      }
    }
  }

  frontmatter += '---\n';

  return frontmatter;
}

/**
 * Generate source page content
 */
export function generateSourcePageContent(
  title: string,
  tldr: string,
  keyPoints: string[],
  evidence: string[],
  impacts: string[],
  contradictions: string[],
  nextActions: string[]
): string {
  let content = `# ${title}\n\n`;
  content += `## TL;DR\n${tldr}\n\n`;
  content += `## Punti chiave\n`;
  for (const point of keyPoints) {
    content += `- ${point}\n`;
  }
  content += '\n';

  if (evidence.length > 0) {
    content += `## Evidenze estratte\n`;
    for (const ev of evidence) {
      content += `- ${ev}\n`;
    }
    content += '\n';
  }

  if (impacts.length > 0) {
    content += `## Impatti sulla wiki\n`;
    for (const impact of impacts) {
      content += `- ${impact}\n`;
    }
    content += '\n';
  }

  if (contradictions.length > 0 || nextActions.length > 0) {
    content += `## Contraddizioni e incertezze\n`;
    if (contradictions.length > 0) {
      for (const c of contradictions) {
        content += `- ${c}\n`;
      }
    } else {
      content += `- Nessuna contraddizione interna alla fonte.\n`;
    }
    content += '\n';
  }

  if (nextActions.length > 0) {
    content += `## Azioni successive\n`;
    for (const action of nextActions) {
      content += `- ${action}\n`;
    }
  }

  return content;
}

/**
 * Generate concept page content
 */
export function generateConceptPageContent(
  name: string,
  definition: string,
  whyItMatters: string,
  rules: string[],
  evidence: string[],
  connections: string[],
  contradictions: string[]
): string {
  let content = `# ${name}\n\n`;
  content += `## Definizione\n${definition}\n\n`;
  content += `## Perché conta\n${whyItMatters}\n\n`;

  if (rules.length > 0) {
    content += `## Regole operative\n`;
    for (const rule of rules) {
      content += `- ${rule}\n`;
    }
    content += '\n';
  }

  if (evidence.length > 0) {
    content += `## Evidenze\n`;
    for (const ev of evidence) {
      content += `- ${ev}\n`;
    }
    content += '\n';
  }

  if (connections.length > 0) {
    content += `## Collegamento entità\n`;
    for (const conn of connections) {
      content += `- ${conn}\n`;
    }
    content += '\n';
  }

  if (contradictions.length > 0) {
    content += `## Contraddizioni e limiti\n`;
    for (const c of contradictions) {
      content += `- ${c}\n`;
    }
  }

  return content;
}

/**
 * Generate entity page content
 */
export function generateEntityPageContent(
  name: string,
  definition: string,
  keyFacts: string[],
  features: string[],
  evidence: string[],
  connections: string[],
  contradictions: string[]
): string {
  let content = `# ${name}\n\n`;
  content += `## Definizione\n${definition}\n\n`;

  if (keyFacts.length > 0) {
    content += `## Fatti rilevanti\n`;
    for (const fact of keyFacts) {
      content += `- ${fact}\n`;
    }
    content += '\n';
  }

  if (features.length > 0) {
    content += `## Caratteristiche\n`;
    for (const feature of features) {
      content += `- ${feature}\n`;
    }
    content += '\n';
  }

  if (evidence.length > 0) {
    content += `## Evidenze\n`;
    for (const ev of evidence) {
      content += `- ${ev}\n`;
    }
    content += '\n';
  }

  if (connections.length > 0) {
    content += `## Relazioni\n`;
    for (const conn of connections) {
      content += `- ${conn}\n`;
    }
    content += '\n';
  }

  if (contradictions.length > 0) {
    content += `## Contraddizioni e note\n`;
    for (const c of contradictions) {
      content += `- ${c}\n`;
    }
  }

  return content;
}

/**
 * Generate lint report content
 */
export function generateLintReportContent(
  date: Date,
  scope: string,
  summary: string,
  sections: Array<{ title: string; items: string[] }>
): string {
  const dateStr = formatDate(date);
  let content = `# Lint Report ${dateStr}\n\n`;
  content += `## Scope\n${scope}\n\n`;
  content += `## Esito sintetico\n${summary}\n\n`;

  for (const section of sections) {
    content += `## ${section.title}\n`;
    if (section.items.length === 0) {
      content += `Nessuna problema rilevato.\n`;
    } else {
      for (const item of section.items) {
        content += `- ${item}\n`;
      }
    }
    content += '\n';
  }

  return content;
}