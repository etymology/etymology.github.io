---
title: "A Lexical Family Tree"
excerpt: "What if we tried to construct a word \"family tree\"? What would it look like? What would we learn?"
comments: true
categories: 
    - 
tags:
    - 
---
 Etymologies sometimes a tree depiction of the history of a word, with the headword as the root. (see example below) What would happen if, we tried to generate a network for the entire lexicon? 

### Topology of etymology

Without actually constructing such a network, we can describe the topology of an idealized etymological network.

Taking as the nodes of our network the various meanings of a word, we can trace the usage of that word with the relation "gives rise to" For example,  OFr. "hercier" gives rise to "hearse" and "rehearsal." This relation is irreflexive, as a word cannot descend from itself. Further we may forbid loops, as a word may not descend from one of its descendants. (n.b This implies that the relation is also asymmetric, so we can treat it as directed) Thus, we can succinctly say that

>Def. An _etymological network_ on a corpus C is a directed acyclic graph on a superset of C with the binary relation "gives rise to"

Because it seems likely that there were fewer headwords in ancient languages, we may guess that this graph will look vaguely like a polytree, with its roots being roots in the appropriate proto-language. (For English, mostly Proto-Indo-European) The graph, is likely to have much branching, and a maximum path length of less than ten (average maximal path length probably around five) judging my my experience with the "number of steps" in most etymologies.

I am interested in the connectedness of the graph. If there were two disconnected components, for example, this would tell us that there are two families of words which share no common roots or intermediaries. There are like two lexical families. It's hard for me to say whether such lexical isolates exist. If there are minimally connected families (for example, families which share a single intermediary ancestor) what words are the bridges? These are some of the topological questions that would be answered by the construction of such a network.

### Practical Challenges

While the necessary information is publicly available, it would be prohibitively tedious to compile it by hand. Probably better would would be to scrape it from some standardized etymology source. Unfortunately, it seems that no such source exists. Most etymologies are verbal descriptions, brief histories of words. Another problem is the resolution of conflicting etymologies, and the procuring of sources for the more difficult dead intermediary languages. All of these present significant challenges to the compilation of any substantial and accurate such network. 

Nonetheless, if we only care about investigating the general structure of such a network and restrict ourselves to a fairly small corpus of "modern" words, it should be possible.

As I proof of concept, I plan to compile such a tree by hand. I hope at some point to have time to write a script to scrape and format the data appropriately for the construction of a more substantial network.