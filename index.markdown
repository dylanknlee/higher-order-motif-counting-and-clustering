---
layout: default
---
# Introduction: What are Networks and Motifs?

_**Networks**_ are a data structure widely popular across all scientific domains to visualize and represent interconnected systems of data. 
Whether it be linked neurons synapsing in the brain, users who follow each other on social media, or cities linked by flights, networks
have been increasingly useful to analyze and deepen our understanding of the relationships between virtually all facets of our everyday life!

While we often regard networks to be built upon nodes joined together by edges, we may find it useful to look at smaller subgraphs instead.
Rather than considering individual nodes to be the primary unit of analysis, we focused on substructures known as _**motifs**_, which for our 
project specifically, are triangular patterns between three separate nodes linked by edges which vary in number and direction.

Shown below is a collection of all the observed motifs analyzed for this project:

![Motifs](assets/motifs.png)

_**But why would we want to utilize motifs instead of nodes?**_

Depending on the domain of inquiry, certain motifs can emerge to become signficantly relevant in certain contexts. For instance, the first seven
motifs are prevalent in social network analysis, while wedges such as the last five motifs are used when studying patterns in air traffic between 
cities. 

Often times, we want to cluster networks to classify nodes into distinct sub-communities to either understand key characteristics about certain 
categories of data, or to help make future predictions regarding unseen data in the future. While much scientific inquiry has been done about 
clustering networks both accurately and efficiently on the level of nodes, little investigation has been done regarding clustering on a higher-order 
level of motifs, which is the primary motivation behind this project.

In exploring higher-order clustering of networks on the motif level, we hope that this endeavor could deepen and enrich pre-existing analyses for any 
domain that employs the usage of graphs.

# Motif Counting

A preliminary step we must take before performing motif clustering is to count the number of occurrences of a desired motif in the given network.

# Spectral Clustering Algorithms

## Algorithm 1

## Algorithm 2

# Network Sampling

# Results and Conclusions

_In progress! :)_

## References

_**Higher order orginazation of complex networks**_ \\
Austin R. Benson, David F. Gleich, and Jure Leskovec (July 7, 2016)

_**Supplementary Materials for Higher-order organization of complex networks**_ \\
Austin R. Benson, David F. Gleich, and Jure Leskovec (July 1, 2016)

## Acknowledgments

We would like to thank _**Barna Saha**_ for her mentorship and advisory throughout our endeavor, _**Suraj Rampure**_ for
overseeing all the administrative and logistical overhead, and finally the _**Halıcıoğlu Data Science Institute**_ in making this 
project possible.