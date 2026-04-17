---
title: "Multi-agent system"
source: "https://en.wikipedia.org/wiki/Multi-agent_system"
author:
  - "[[Wikipedia]]"
published: 2004-08-29
created: 2026-04-17
description:
tags:
  - "clippings"
---
![](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/IntelligentAgent-SimpleReflex.png/250px-IntelligentAgent-SimpleReflex.png)

Simple reflex agent

![](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b7/IntelligentAgent-Learning.svg/250px-IntelligentAgent-Learning.svg.png)

Learning agent

A **multi-agent system** (**MAS**) or "self-organized system" is a computational system composed of multiple interacting [intelligent agents](https://en.wikipedia.org/wiki/Intelligent_agent "Intelligent agent").[^1] [^2] [^3] Multi-agent systems can solve problems that are difficult or impossible for an individual agent or a [monolithic system](https://en.wikipedia.org/wiki/Monolithic_system "Monolithic system") to solve.[^4] Intelligence may include [methodic](https://en.wikipedia.org/wiki/Scientific_method "Scientific method"), [functional](https://en.wikipedia.org/wiki/Function_\(computer_science\) "Function (computer science)"), [procedural](https://en.wikipedia.org/wiki/Algorithm "Algorithm") approaches, [algorithmic](https://en.wikipedia.org/wiki/Algorithm "Algorithm") [search](https://en.wikipedia.org/wiki/Search_algorithm "Search algorithm") or [reinforcement learning](https://en.wikipedia.org/wiki/Reinforcement_learning "Reinforcement learning").[^5] With advancements in [large language models](https://en.wikipedia.org/wiki/Large_language_model "Large language model") (LLMs), LLM-based multi-agent systems have emerged as a new area of research, enabling more sophisticated interactions and coordination among agents.[^6]

Despite considerable overlap, a multi-agent system is not always the same as an [agent-based model](https://en.wikipedia.org/wiki/Agent-based_model "Agent-based model") (ABM). The goal of an ABM is to search for explanatory insight into the collective behavior of agents (which do not necessarily need to be "intelligent") obeying simple rules, typically in natural systems, rather than in solving specific practical or engineering problems. The terminology of ABM tends to be used more often in the science, and MAS in engineering and technology.[^7] Applications where multi-agent systems research may deliver an appropriate approach include online trading,[^8] disaster response,[^9] [^10] target surveillance [^11] and social structure modelling.[^12]

## Concept

Multi-agent systems consist of agents and their [environment](https://en.wikipedia.org/wiki/Biophysical_environment "Biophysical environment"). Typically, research on multi-agent systems refers to [software agents](https://en.wikipedia.org/wiki/Software_agent "Software agent"). However, the agents in a multi-agent system could equally well be robots, humans, or human teams, and may consist of combined human-agent teams.

Agents can be divided into types spanning simple to complex. Categories include:

- Passive agents [^13] or "agent without goals" (such as obstacle, apple or key in any simple simulation)
- Active agents [^13] with simple goals (like birds in flocking, or wolf–sheep in [prey-predator model](https://en.wikipedia.org/wiki/Lotka%E2%80%93Volterra "Lotka–Volterra"))
- Cognitive agents, with beliefs, desires, intentions, and commitments processed by logical, probabilistic, and neural network-based reasoning

Agent environments can be divided into:

- Virtual
- Discrete
- Continuous

Agent environments can also be organized according to properties such as accessibility (whether it is possible to gather complete information about the environment), determinism (whether an action causes a definite effect), dynamics (how many entities influence the environment in the moment), discreteness (whether the number of possible actions in the environment is finite), episodicity (whether agent actions in certain time periods influence other periods),[^14] and dimensionality (whether spatial characteristics are important factors of the environment and the agent considers space in its decision making).[^15] Agent actions are typically mediated via an appropriate middleware. This middleware offers a first-class design abstraction for multi-agent systems, providing means to govern resource access and agent coordination.[^16]

### Characteristics

The agents in a multi-agent system have several important characteristics:[^17]

- Autonomy: agents are at least partially independent, self-aware, [autonomous](https://en.wikipedia.org/wiki/Autonomous_agent "Autonomous agent")
- Local views: no agent has a full global view, or the system is too complex for an agent to exploit such knowledge
- Decentralization: no agent is designated as controlling (or the system is effectively reduced to a monolithic system) [^18]

### Self-organisation and self-direction

Multi-agent systems can manifest [self-organisation](https://en.wikipedia.org/wiki/Self-organisation "Self-organisation") as well as self-direction and other [control paradigms](https://en.wikipedia.org/wiki/Control_theory "Control theory") and related complex behaviors even when the individual strategies of all their agents are simple. When agents can share knowledge using any agreed language, within the constraints of the system's communication protocol, the approach may lead to a common improvement. Example languages are [Knowledge Query Manipulation Language](https://en.wikipedia.org/wiki/KQML "KQML") (KQML) or [Agent Communication Language](https://en.wikipedia.org/wiki/Agent_Communication_Language "Agent Communication Language") (ACL).

### Decision-Making

Decision protocols in multi-agent systems refer to the structured rules and procedures that agents follow to reach collective decisions or agreements. Such protocols specify how agents share information, negotiate, and resolve conflicts, ensuring coordinated behavior and effective joint actions. Decision protocols can range from [voting](https://en.wikipedia.org/wiki/Voting "Voting") mechanisms to [consensus](https://en.wikipedia.org/wiki/Consensus_decision-making "Consensus decision-making") -building algorithms, and they significantly influence the efficiency and reliability of multi-agent interactions.[^19]

### System paradigms

Many MAS are implemented in computer simulations, stepping the system through discrete "time steps". The MAS components communicate typically using a weighted request matrix, e.g.

```
Speed-VERY_IMPORTANT: min=45 mph, 
Path length-MEDIUM_IMPORTANCE: max=60 expectedMax=40, 
Max-Weight-UNIMPORTANT 
Contract Priority-REGULAR
```

and a weighted response matrix, e.g.

```
Speed-min:50 but only if weather sunny, 
Path length:25 for sunny / 46 for rainy
Contract Priority-REGULAR
note – ambulance will override this priority and you'll have to wait
```

A challenge-response-contract scheme is common in MAS systems, where

- First a **"** Who can?**"** question is distributed.
- Only the relevant components respond: **"** I can, at this price **"**.
- Finally, a contract is set up, usually in several short communication steps between sides,

also considering other components, evolving "contracts" and the restriction sets of the component algorithms.

Another paradigm commonly used with MAS is the " [pheromone](https://en.wikipedia.org/wiki/Pheromone "Pheromone") ", where components leave information for other nearby components. These pheromones may evaporate/concentrate with time, that is their values may decrease (or increase).

### Properties

MAS tend to find the best solution for their problems without intervention. There is high similarity here to physical phenomena, such as energy minimizing, where physical objects tend to reach the lowest energy possible within the physically constrained world. For example: many of the cars entering a metropolis in the morning will be available for leaving that same metropolis in the evening.

The systems also tend to prevent propagation of faults, self-recover and be fault tolerant, mainly due to the redundancy of components.

## Research

The study of multi-agent systems is "concerned with the development and analysis of sophisticated [AI](https://en.wikipedia.org/wiki/Artificial_intelligence "Artificial intelligence") problem-solving and control architectures for both single-agent and multiple-agent systems." [^20] Research topics include:

- agent-oriented software engineering
- beliefs, desires, and intentions ([BDI](https://en.wikipedia.org/wiki/BDI_software_agent "BDI software agent"))
- [cooperation and coordination](https://en.wikipedia.org/wiki/Consensus_dynamics "Consensus dynamics")
- [distributed constraint optimization](https://en.wikipedia.org/wiki/Distributed_constraint_optimization "Distributed constraint optimization") (DCOPs)
- organization
- communication
- negotiation
- [distributed problem solving](https://en.wikipedia.org/wiki/Cooperative_distributed_problem_solving "Cooperative distributed problem solving")
- [multi-agent learning](https://en.wikipedia.org/wiki/Multi-agent_learning "Multi-agent learning") [^21]
- [agent mining](https://en.wikipedia.org/wiki/Agent_mining "Agent mining")
- scientific communities (e.g., on biological flocking, language evolution, and economics) [^22] [^23]
- dependability and fault-tolerance
- robotics,[^24] multi-robot systems (MRS), robotic clusters
- multi-agent systems also present possible applications in microrobotics,[^25] where the physical interaction between the agents are exploited to perform complex tasks such as manipulation and assembly of passive components.
- language model-based multi-agent systems [^6]

A MAS involves more than just the design of an intelligent system. It also provides insights and understanding about interactions among humans, as they organize themselves into various groups, committees, societies, and economies in order to improve their lives. For example, economists have been studying multiple agents for more than two hundred years, ever since Adam Smith in the eighteenth century, with the goal of being able to understand and predict economies. Economics provides ways to characterize masses of agents. and these are useful for DAI. But in return, DAI provides a means to construct artificial economies that can test economists’ theories before, rather than after, they are applied.

## Frameworks

Frameworks have emerged that implement common standards (such as the [FIPA](https://en.wikipedia.org/wiki/Foundation_for_Intelligent_Physical_Agents "Foundation for Intelligent Physical Agents") and [OMG](https://en.wikipedia.org/wiki/Object_Management_Group "Object Management Group") MASIF standards).[^26] These frameworks e.g. [JADE](https://en.wikipedia.org/wiki/Java_Agent_Development_Framework "Java Agent Development Framework"), save time and aid in the standardization of MAS development.[^27]

Currently though, no standard is actively maintained from FIPA or OMG. Efforts for further development of software agents in industrial context are carried out in [IEEE](https://en.wikipedia.org/wiki/Institute_of_Electrical_and_Electronics_Engineers "Institute of Electrical and Electronics Engineers") IES technical committee on Industrial Agents.[^28]

With advancements in [large language models](https://en.wikipedia.org/wiki/Large_language_model "Large language model") (LLMs) such as [ChatGPT](https://en.wikipedia.org/wiki/ChatGPT "ChatGPT"), LLM-based multi-agent frameworks, such as CAMEL,[^29] [^6] have emerged as a new paradigm for developing multi-agent applications. Recent work has shown that such debate-oriented systems vary in their orchestration (e.g., discussion paradigms [^30]). The MALLM framework is used to systematically evaluate possible configurations of frameworks.[^31]

## Applications

MAS have not only been applied in academic research, but also in industry.[^32] MAS are applied in the real world to graphical applications such as computer games. Agent systems have been used in films.[^33] It is widely advocated for use in networking and mobile technologies, to achieve automatic and dynamic load balancing, high scalability and self-healing networks. They are being used for coordinated defence systems.

Other applications [^34] include [transportation](https://en.wikipedia.org/wiki/Transportation "Transportation"),[^35] logistics,[^36] graphics, manufacturing, [power system](https://en.wikipedia.org/wiki/Power_system "Power system"),[^37] [smartgrids](https://en.wikipedia.org/wiki/Smartgrids "Smartgrids"),[^38] and the [GIS](https://en.wikipedia.org/wiki/Geographic_information_system "Geographic information system").

Also, [Multi-agent Systems Artificial Intelligence](https://en.wikipedia.org/wiki/Distributed_artificial_intelligence#Agents_and_Multi-agent_systems "Distributed artificial intelligence") (MAAI) are used for simulating societies, the purpose thereof being helpful in the fields of climate, energy, [epidemiology](https://en.wikipedia.org/wiki/Epidemiology "Epidemiology"), [conflict management](https://en.wikipedia.org/wiki/Conflict_management "Conflict management"), child abuse,....[^39]

Some organisations working on using multi-agent system models include Center for Modelling Social Systems,[^40] Centre for Research in Social Simulation,[^41] Centre for Policy Modelling, Society for Modelling and Simulation International.[^39]

Vehicular traffic with controlled autonomous vehicles can be modelling as a multi-agent system involving crowd dynamics.[^42]

Hallerbach et al. discussed the application of agent-based approaches for the development and validation of [automated driving systems](https://en.wikipedia.org/wiki/Vehicular_automation "Vehicular automation") via a digital twin of the vehicle-under-test and microscopic traffic simulation based on independent agents.[^43] [Waymo](https://en.wikipedia.org/wiki/Waymo "Waymo") has created a multi-agent simulation environment Carcraft to test algorithms for [self-driving cars](https://en.wikipedia.org/wiki/Self-driving_car "Self-driving car").[^44] [^45] It simulates traffic interactions between human drivers, pedestrians and automated vehicles. People's behavior is imitated by artificial agents based on data of real human behavior.

[^1]: Singh, Munindar P. (1994). *Multiagent Systems: A Theoretical Framework for Intentions, Know-How, and Communications*. Vol. 799. Springer-Verlag, Lecture Notes in Computer Science. [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [0-387-58026-3](https://en.wikipedia.org/wiki/Special:BookSources/0-387-58026-3 "Special:BookSources/0-387-58026-3").

[^2]: Yoav Shoham, Kevin Leyton-Brown. *Multiagent Systems: Algorithmic, Game-Theoretic, and Logical Foundations.* Cambridge University Press, 2009. [http://www.masfoundations.org/](http://www.masfoundations.org/)

[^3]: H. Pan; M. Zahmatkesh; F. Rekabi-Bana; F. Arvin; J. Hu " [T-STAR: Time-Optimal Swarm Trajectory Planning for Quadrotor Unmanned Aerial Vehicles](https://ieeexplore.ieee.org/document/10965835) " IEEE Transactions on Intelligent Transportation Systems, 2025.

[^4]: Hu, J.; Turgut, A.; Lennox, B.; Arvin, F., " [Robust Formation Coordination of Robot Swarms with Nonlinear Dynamics and Unknown Disturbances: Design and Experiments](https://ieeexplore.ieee.org/abstract/document/9409965) " IEEE Transactions on Circuits and Systems II: Express Briefs, 2021.

[^5]: Stefano V. Albrecht, Filippos Christianos, Lukas Schäfer. *Multi-Agent Reinforcement Learning: Foundations and Modern Approaches.* MIT Press, 2024. [https://www.marl-book.com/](https://www.marl-book.com/)

[^6]: Li, Guohao (2023). ["Camel: Communicative agents for "mind" exploration of large language model society"](https://proceedings.neurips.cc/paper_files/paper/2023/file/a3621ee907def47c1b952ade25c67698-Paper-Conference.pdf) (PDF). *Advances in Neural Information Processing Systems*. **36**: 51991–52008. [arXiv](https://en.wikipedia.org/wiki/ArXiv_\(identifier\) "ArXiv (identifier)"):[2303.17760](https://arxiv.org/abs/2303.17760). [S2CID](https://en.wikipedia.org/wiki/S2CID_\(identifier\) "S2CID (identifier)") [257900712](https://api.semanticscholar.org/CorpusID:257900712).

[^7]: Niazi, Muaz; Hussain, Amir (2011). ["Agent-based Computing from Multi-agent Systems to Agent-Based Models: A Visual Survey"](https://www.researchgate.net/publication/220365334) (PDF). *Scientometrics*. **89** (2): 479–499. [arXiv](https://en.wikipedia.org/wiki/ArXiv_\(identifier\) "ArXiv (identifier)"):[1708.05872](https://arxiv.org/abs/1708.05872). [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1007/s11192-011-0468-9](https://doi.org/10.1007%2Fs11192-011-0468-9). [hdl](https://en.wikipedia.org/wiki/Hdl_\(identifier\) "Hdl (identifier)"):[1893/3378](https://hdl.handle.net/1893%2F3378). [S2CID](https://en.wikipedia.org/wiki/S2CID_\(identifier\) "S2CID (identifier)") [17934527](https://api.semanticscholar.org/CorpusID:17934527).

[^8]: Rogers, Alex; David, E.; Schiff, J.; Jennings, N.R. (2007). ["The Effects of Proxy Bidding and Minimum Bid Increments within eBay Auctions"](https://web.archive.org/web/20100402101304/http://eprints.ecs.soton.ac.uk/12716/). *ACM Transactions on the Web*. **1** (2): 9–es. [CiteSeerX](https://en.wikipedia.org/wiki/CiteSeerX_\(identifier\) "CiteSeerX (identifier)") [10.1.1.65.4539](https://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.65.4539). [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1145/1255438.1255441](https://doi.org/10.1145%2F1255438.1255441). [S2CID](https://en.wikipedia.org/wiki/S2CID_\(identifier\) "S2CID (identifier)") [207163424](https://api.semanticscholar.org/CorpusID:207163424). Archived from [the original](http://eprints.ecs.soton.ac.uk/12716/) on April 2, 2010. Retrieved March 18, 2008.

[^9]: Schurr, Nathan; Marecki, Janusz; Tambe, Milind; Scerri, Paul; Kasinadhuni, Nikhil; Lewis, J.P. (2005). ["The Future of Disaster Response: Humans Working with Multiagent Teams using DEFACTO"](https://aaai.org/papers/0002-ss05-01-002-the-future-of-disaster-response-humans-working-with-multiagent-teams-using-defacto). [Archived](https://web.archive.org/web/20130603165342/http://teamcore.usc.edu/papers/2005/SS105SchurrN.pdf) (PDF) from the original on June 3, 2013. Retrieved January 8, 2024.

[^10]: Genc, Zulkuf; et al. (2013). ["Agent-Based Information Infrastructure for Disaster Management"](http://www.gdmc.nl/gi4dmdocs/Gi4DM_2012_Genc.pdf) (PDF). *Intelligent Systems for Crisis Management*. Lecture Notes in Geoinformation and Cartography. pp. 349–355. [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1007/978-3-642-33218-0\_26](https://doi.org/10.1007%2F978-3-642-33218-0_26). [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [978-3-642-33217-3](https://en.wikipedia.org/wiki/Special:BookSources/978-3-642-33217-3 "Special:BookSources/978-3-642-33217-3").

[^11]: Hu, Junyan; Bhowmick, Parijat; Lanzon, Alexander (2020). ["Distributed Adaptive Time-Varying Group Formation Tracking for Multiagent Systems With Multiple Leaders on Directed Graphs"](https://doi.org/10.1109%2FTCNS.2019.2913619). *IEEE Transactions on Control of Network Systems*. **7**: 140–150. [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1109/TCNS.2019.2913619](https://doi.org/10.1109%2FTCNS.2019.2913619). [S2CID](https://en.wikipedia.org/wiki/S2CID_\(identifier\) "S2CID (identifier)") [149609966](https://api.semanticscholar.org/CorpusID:149609966).

[^12]: [Sun, Ron](https://en.wikipedia.org/wiki/Ron_Sun "Ron Sun"); Naveh, Isaac (June 30, 2004). ["Simulating Organizational Decision-Making Using a Cognitively Realistic Agent Model"](http://jasss.soc.surrey.ac.uk/7/3/5.html). *Journal of Artificial Societies and Social Simulation*.

[^13]: Kubera, Yoann; Mathieu, Philippe; Picault, Sébastien (2010), ["Everything can be Agent!"](http://www.lifl.fr/SMAC/publications/pdf/aamas2010-everything.pdf) (PDF), *Proceedings of the Ninth International Joint Conference on Autonomous Agents and Multi-Agent Systems (AAMAS'2010)*: 1547–1548

[^14]: [Russell, Stuart J.](https://en.wikipedia.org/wiki/Stuart_J._Russell "Stuart J. Russell"); [Norvig, Peter](https://en.wikipedia.org/wiki/Peter_Norvig "Peter Norvig") (2003), [*Artificial Intelligence: A Modern Approach*](http://aima.cs.berkeley.edu/) (2nd ed.), Upper Saddle River, New Jersey: Prentice Hall, [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [0-13-790395-2](https://en.wikipedia.org/wiki/Special:BookSources/0-13-790395-2 "Special:BookSources/0-13-790395-2")

[^15]: Salamon, Tomas (2011). [*Design of Agent-Based Models*](http://www.designofagentbasedmodels.info/). Repin: Bruckner Publishing. p. 22. [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [978-80-904661-1-1](https://en.wikipedia.org/wiki/Special:BookSources/978-80-904661-1-1 "Special:BookSources/978-80-904661-1-1").

[^16]: Weyns, Danny; Omicini, Amdrea; Odell, James (2007). "Environment as a first-class abstraction in multiagent systems". *Autonomous Agents and Multi-Agent Systems*. **14** (1): 5–30. [CiteSeerX](https://en.wikipedia.org/wiki/CiteSeerX_\(identifier\) "CiteSeerX (identifier)") [10.1.1.154.4480](https://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.154.4480). [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1007/s10458-006-0012-0](https://doi.org/10.1007%2Fs10458-006-0012-0). [S2CID](https://en.wikipedia.org/wiki/S2CID_\(identifier\) "S2CID (identifier)") [13347050](https://api.semanticscholar.org/CorpusID:13347050).

[^17]: Wooldridge, Michael (2002). *An Introduction to MultiAgent Systems*. [John Wiley & Sons](https://en.wikipedia.org/wiki/John_Wiley_%26_Sons "John Wiley & Sons"). p. 366. [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [978-0-471-49691-5](https://en.wikipedia.org/wiki/Special:BookSources/978-0-471-49691-5 "Special:BookSources/978-0-471-49691-5").

[^18]: Panait, Liviu; Luke, Sean (2005). ["Cooperative Multi-Agent Learning: The State of the Art"](http://cs.gmu.edu/~eclab/papers/panait05cooperative.pdf) (PDF). *Autonomous Agents and Multi-Agent Systems*. **11** (3): 387–434. [CiteSeerX](https://en.wikipedia.org/wiki/CiteSeerX_\(identifier\) "CiteSeerX (identifier)") [10.1.1.307.6671](https://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.307.6671). [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1007/s10458-005-2631-2](https://doi.org/10.1007%2Fs10458-005-2631-2). [S2CID](https://en.wikipedia.org/wiki/S2CID_\(identifier\) "S2CID (identifier)") [19706](https://api.semanticscholar.org/CorpusID:19706).

[^19]: Kaesberg, Lars Benedikt; Becker, Jonas; Wahle, Jan Philip; Ruas, Terry; Gipp, Bela (July 1, 2025). Che, Wanxiang; Nabende, Joyce; Shutova, Ekaterina; Pilehvar, Mohammad Taher (eds.). ["Voting or Consensus? Decision-Making in Multi-Agent Debate"](https://aclanthology.org/2025.findings-acl.606/). *Findings of the Association for Computational Linguistics: ACL 2025*. Vienna, Austria: Association for Computational Linguistics: 11640–11671. [arXiv](https://en.wikipedia.org/wiki/ArXiv_\(identifier\) "ArXiv (identifier)"):[2502.19130](https://arxiv.org/abs/2502.19130). [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.18653/v1/2025.findings-acl.606](https://doi.org/10.18653%2Fv1%2F2025.findings-acl.606). [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [979-8-89176-256-5](https://en.wikipedia.org/wiki/Special:BookSources/979-8-89176-256-5 "Special:BookSources/979-8-89176-256-5").

[^20]: ["The Multi-Agent Systems Lab"](http://mas.cs.umass.edu/). [University of Massachusetts Amherst](https://en.wikipedia.org/wiki/University_of_Massachusetts_Amherst "University of Massachusetts Amherst"). Retrieved October 16, 2009.

[^21]: Albrecht, Stefano; Stone, Peter (2017), "Multiagent Learning: Foundations and Recent Trends. Tutorial", [*IJCAI-17 conference*](http://www.cs.utexas.edu/~larg/ijcai17_tutorial/multiagent_learning.pdf) (PDF)

[^22]: Cucker, Felipe; [Steve Smale](https://en.wikipedia.org/wiki/Stephen_Smale "Stephen Smale") (2007). ["The Mathematics of Emergence"](http://ttic.uchicago.edu/~smale/papers/math-of-emergence.pdf) (PDF). *Japanese Journal of Mathematics*. **2**: 197–227. [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1007/s11537-007-0647-x](https://doi.org/10.1007%2Fs11537-007-0647-x). [S2CID](https://en.wikipedia.org/wiki/S2CID_\(identifier\) "S2CID (identifier)") [2637067](https://api.semanticscholar.org/CorpusID:2637067). Retrieved June 9, 2008.

[^23]: Shen, Jackie (Jianhong) (2008). ["Cucker–Smale Flocking under Hierarchical Leadership"](http://scitation.aip.org/getabs/servlet/GetabsServlet?prog=normal&id=SMJMAP000068000003000694000001&idtype=cvips&gifs=yes). *SIAM J. Appl. Math*. **68** (3): 694–719. [arXiv](https://en.wikipedia.org/wiki/ArXiv_\(identifier\) "ArXiv (identifier)"):[q-bio/0610048](https://arxiv.org/abs/q-bio/0610048). [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1137/060673254](https://doi.org/10.1137%2F060673254). [S2CID](https://en.wikipedia.org/wiki/S2CID_\(identifier\) "S2CID (identifier)") [14655317](https://api.semanticscholar.org/CorpusID:14655317). Retrieved June 9, 2008.

[^24]: Ahmed, S.; Karsiti, M.N. (2007), "A testbed for control schemes using multi agent nonholonomic robots", [*2007 IEEE International Conference on Electro/Information Technology*](http://eprints.utp.edu.my/320/), p. 459, [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1109/EIT.2007.4374547](https://doi.org/10.1109%2FEIT.2007.4374547), [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [978-1-4244-0940-2](https://en.wikipedia.org/wiki/Special:BookSources/978-1-4244-0940-2 "Special:BookSources/978-1-4244-0940-2"), [S2CID](https://en.wikipedia.org/wiki/S2CID_\(identifier\) "S2CID (identifier)") [2734931](https://api.semanticscholar.org/CorpusID:2734931)

[^25]: Yang, Lidong; Li, Zhang (2021). "Motion control in magnetic microrobotics: From individual and multiple robots to swarms". *Annual Review of Control, Robotics, and Autonomous Systems*. **4**: 509–534. [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1146/annurev-control-032720-104318](https://doi.org/10.1146%2Fannurev-control-032720-104318). [S2CID](https://en.wikipedia.org/wiki/S2CID_\(identifier\) "S2CID (identifier)") [228892228](https://api.semanticscholar.org/CorpusID:228892228).

[^26]: ["OMG Document – orbos/97-10-05 (Update of Revised MAF Submission)"](https://www.omg.org/cgi-bin/doc?orbos/97-10-05). *www.omg.org*. Retrieved February 19, 2019.

[^27]: Ahmed, Salman; Karsiti, Mohd N.; Agustiawan, Herman (2007). ["A development framework for collaborative robots using feedback control"](https://www.researchgate.net/publication/238431442). Retrieved January 8, 2024.

[^28]: ["IEEE IES Technical Committee on Industrial Agents (TC-IA)"](https://tcia.ieee-ies.org/). *tcia.ieee-ies.org*. Retrieved February 19, 2019.

[^29]: ["CAMEL: Finding the Scaling Law of Agents. The first and the best multi-agent framework"](https://github.com/camel-ai/camel/). *[GitHub](https://en.wikipedia.org/wiki/GitHub "GitHub")*.

[^30]: Yin, Zhangyue; Sun, Qiushi; Chang, Cheng; Guo, Qipeng; Dai, Junqi; Huang, Xuanjing; Qiu, Xipeng (December 2023). ["Exchange‑of‑Thought: Enhancing Large Language Model Capabilities through Cross‑Model Communication"](https://aclanthology.org/2023.emnlp-main.936/). *Proceedings of the 2023 Conference on Empirical Methods in Natural Language Processing*. Singapore: Association for Computational Linguistics. pp. 15135–15153. [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.18653/v1/2023.emnlp-main.936](https://doi.org/10.18653%2Fv1%2F2023.emnlp-main.936).

[^31]: Becker, Jonas; Kaesberg, Lars Benedikt; Bauer, Niklas; Wahle, Jan Philip; Ruas, Terry; Gipp, Bela (November 2025). ["MALLM: Multi‑Agent Large Language Models Framework"](https://aclanthology.org/2025.emnlp-demos.29/). *Proceedings of the 2025 Conference on Empirical Methods in Natural Language Processing: System Demonstrations*. Suzhou, China: Association for Computational Linguistics. pp. 418–439. [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.18653/v1/2025.emnlp-demos.29](https://doi.org/10.18653%2Fv1%2F2025.emnlp-demos.29).

[^32]: Leitão, Paulo; Karnouskos, Stamatis (March 26, 2015). *Industrial agents: emerging applications of software agents in industry*. Leitão, Paulo,, Karnouskos, Stamatis. Amsterdam, Netherlands. [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [978-0128003411](https://en.wikipedia.org/wiki/Special:BookSources/978-0128003411 "Special:BookSources/978-0128003411"). [OCLC](https://en.wikipedia.org/wiki/OCLC_\(identifier\) "OCLC (identifier)") [905853947](https://search.worldcat.org/oclc/905853947).

[^33]: ["Film showcase"](http://www.massivesoftware.com/film.html). [MASSIVE](https://en.wikipedia.org/wiki/Massive_\(software\) "Massive (software)"). Retrieved April 28, 2012.

[^34]: Leitao, Paulo; Karnouskos, Stamatis; Ribeiro, Luis; Lee, Jay; Strasser, Thomas; Colombo, Armando W. (2016). ["Smart Agents in Industrial Cyber–Physical Systems"](http://urn.kb.se/resolve?urn=urn:nbn:se:liu:diva-128744). *Proceedings of the IEEE*. **104** (5): 1086–1101. [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1109/JPROC.2016.2521931](https://doi.org/10.1109%2FJPROC.2016.2521931). [hdl](https://en.wikipedia.org/wiki/Hdl_\(identifier\) "Hdl (identifier)"):[10198/15438](https://hdl.handle.net/10198%2F15438). [ISSN](https://en.wikipedia.org/wiki/ISSN_\(identifier\) "ISSN (identifier)") [0018-9219](https://search.worldcat.org/issn/0018-9219). [S2CID](https://en.wikipedia.org/wiki/S2CID_\(identifier\) "S2CID (identifier)") [579475](https://api.semanticscholar.org/CorpusID:579475).

[^35]: Xiao-Feng Xie, S. Smith, G. Barlow. [Schedule-driven coordination for real-time traffic network control](http://www.wiomax.com/team/xie/paper/ICAPS12.pdf). International Conference on Automated Planning and Scheduling (ICAPS), São Paulo, Brazil, 2012: 323–331.

[^36]: Máhr, T. S.; Srour, J.; De Weerdt, M.; Zuidwijk, R. (2010). "Can agents measure up? A comparative study of an agent-based and on-line optimization approach for a drayage problem with uncertainty". *Transportation Research Part C: Emerging Technologies*. **18** (1): 99–119. [Bibcode](https://en.wikipedia.org/wiki/Bibcode_\(identifier\) "Bibcode (identifier)"):[2010TRPC...18...99M](https://ui.adsabs.harvard.edu/abs/2010TRPC...18...99M). [CiteSeerX](https://en.wikipedia.org/wiki/CiteSeerX_\(identifier\) "CiteSeerX (identifier)") [10.1.1.153.770](https://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.153.770). [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1016/j.trc.2009.04.018](https://doi.org/10.1016%2Fj.trc.2009.04.018).

[^37]: Kazemi, Hamidreza; Liasi, Sahand; Sheikh-El-Eslami, Mohammadkazem (November 2018). ["Generation Expansion Planning Considering Investment Dynamic of Market Participants Using Multi-agent System"](https://www.researchgate.net/publication/334765661). *2018 Smart Grid Conference (SGC)*. pp. 1–6. [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1109/SGC.2018.8777904](https://doi.org/10.1109%2FSGC.2018.8777904). [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [978-1-7281-1138-4](https://en.wikipedia.org/wiki/Special:BookSources/978-1-7281-1138-4 "Special:BookSources/978-1-7281-1138-4"). Retrieved January 8, 2024.

[^38]: Singh, Vijay; Samuel, Paulson (June 6, 2017). ["Distributed Multi -Agent System Based Load Frequency Control for Multi- Area Power System in Smart Grid"](https://www.researchgate.net/publication/312304154). *IEEE Transactions on Industrial Electronics*. **64** (6): 5151–5160. [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1109/TIE.2017.2668983](https://doi.org/10.1109%2FTIE.2017.2668983). Retrieved January 8, 2024.

[^39]: ["AI can predict your future behaviour with powerful new simulations"](https://www.newscientist.com/article/mg24332500-800-ai-can-predict-your-future-behaviour-with-powerful-new-simulations/). *New Scientist*.

[^40]: ["Center for Modeling Social Systems - Norce"](https://www.norceresearch.no/en/research-group/cmss). *NORCE Norwegian Research Centre*. Retrieved April 13, 2025.

[^41]: ["Centre for Research in Social Simulation – A multidisciplinary centre bringing together the social sciences and agent-based modelling to promote and support the use of social simulation in research in the human sciences"](https://cress.soc.surrey.ac.uk/cresswp/). Retrieved April 13, 2025.

[^42]: Gong, Xiaoqian; Herty, Michael; Piccoli, Benedetto; Visconti, Giuseppe (May 3, 2023). ["Crowd Dynamics: Modeling and Control of Multiagent Systems"](https://doi.org/10.1146%2Fannurev-control-060822-123629). *Annual Review of Control, Robotics, and Autonomous Systems*. **6** (1): 261–282. [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1146/annurev-control-060822-123629](https://doi.org/10.1146%2Fannurev-control-060822-123629). [ISSN](https://en.wikipedia.org/wiki/ISSN_\(identifier\) "ISSN (identifier)") [2573-5144](https://search.worldcat.org/issn/2573-5144).

[^43]: Hallerbach, S.; Xia, Y.; Eberle, U.; Koester, F. (2018). ["Simulation-Based Identification of Critical Scenarios for Cooperative and Automated Vehicles"](https://www.researchgate.net/publication/324194968). *SAE International Journal of Connected and Automated Vehicles*. **1** (2). SAE International: 93. [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.4271/2018-01-1066](https://doi.org/10.4271%2F2018-01-1066).

[^44]: Madrigal, Story by Alexis C. ["Inside Waymo's Secret World for Training Self-Driving Cars"](https://www.theatlantic.com/technology/archive/2017/08/inside-waymos-secret-testing-and-simulation-facilities/537648/). *The Atlantic*. Retrieved August 14, 2020.

[^45]: Connors, J.; Graham, S.; Mailloux, L. (2018). "Cyber Synthetic Modeling for Vehicle-to-Vehicle Applications". *In International Conference on Cyber Warfare and Security*. Academic Conferences International Limited: 594-XI.