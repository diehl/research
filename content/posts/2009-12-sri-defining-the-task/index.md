---
title: "Social Relationship Identification: Defining the Task"
date: 2009-12-15T13:51:04-07:00
tags: [Social Relationship Identification]
---
In recent years, informal, online communication has transformed the way we connect and collaborate with others. Through a range of online communication technologies, we are able to enrich existing social relationships and establish new relationships that would otherwise be difficult or impossible to develop offline. Now that storage has become vast and inexpensive, much of this data will be archived for years to come. This provides new opportunities and new challenges.

As networked groups and organizations increasingly leverage online means of communication and collaboration, there is an opportunity to observe the formation and evolution of roles and relationships from the communications archives. Such data provides a rich collection of evidence from which to infer the structure, attributes and dynamics of the underlying social network. Yet numerous challenges emerge as one contends with data that is often ambiguous, incomplete and context-dependent.  

If we wish to analyze the underlying social network that is at least partially represented by a collection of informal, online communications, it is important to think carefully about the data transformations required prior to conducting any type of analysis. At the highest level, we are fundamentally interested in discovering entities and the types of relationships they share. This implies that we must do more than simply adopt the communications (hyper)graph as a surrogate for the social network. Entities can and often do use more than one account online and not all communications relationships are equivalent. In fact, the social network can be thought of as a collection of networks with different relationship types (e.g. friendship, trust, advice, management). Human relations are multi-faceted and context-dependent. Therefore it is important to tease the communications apart and understand what types of relationships are being expressed among the entities.  

As an example, consider the domain of litigation support. In any investigation of corporate malfeasance, it is now commonplace to subpoena email records to look for incriminating evidence. A common tactic in response to such a subpoena is to provide a deluge of email to complicate evidence discovery. The volume and complexity of such data can easily overwhelm analysts attempting to reconstruct the underlying social network. Even with commercially available tools, current practice still requires significant analyst effort.*  

When Lise Getoor and I began to think about this problem several years ago, we envisioned a process for collaborative network discovery where the analyst provides context and the machine learns from that context to aid in the discovery of relevant social relations. To be precise, the task of social relationship identification involves identifying communication relationships that exhibit a given social relation along with specific messages that provide supporting evidence. Within this collaborative process, the analyst ultimately decides whether or not a given social relationship exists between two entities. The role of the machine is to prioritize communication relationships the analyst should consider and messages within each relationship that the analyst should read. By exploiting judgments provided by the analyst along the way, the machine will continuously learn to cue the analyst to relevant relationships and message content. Realizing this capability, as one might imagine, is riddled with challenges.

In the next post, we will consider issues of representation prior to discussing the ranking process in more detail.  Future posts will cover our latest insights that extend beyond what is currently published.  

The original task definition was presented in our AAAI 2007 paper which is available [here](aaai07-final.pdf).

* A colleague related a story where a major consulting firm was hired to aid in the investigation of a European company. For several weeks, a team of consultants manually read emails and coded social relationships among company employees by hand.

[Joint work with Lise Getoor (UMCP), Galileo Namata (UMCP), Jaime Montemayor (JHU/APL) and Mike Pekala (JHU/APL)]
