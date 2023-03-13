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

For this process, we'll utilize two data structures created while pre-processing the raw network dataset: an adjacency list for every node, which
stores all the other nodes it has an edge pointing towards (named _**adj_list_away**_), and similarly another adjacency list for each node which
stores all the edges that begin with other nodes and point towards it (named _**adj_list_in**_).

We then employ the following naive counting algorithm, whose general form is presented here in pseudocode:

```ruby
1.) Iterate through each vertex v1 in adj_list_away
2.) Iterate through each vertex v2 which v1 points to 
    in adj_list_away
3.) Iterate through each vertex v3 which v2 points to 
    in adj_list_away
4.) Check that the number and directions of the iterated
    edges match that of the desired motif
5.) If so, record the edges amongst (v1, v2, v3) as an
    observed instance of the motif       
```
As shown above, our counting method maintains a computation time complexity of O(n^3) by naively iterating through each possible path of node triples
in the network to check for any observed instance of the desired motif, which we aim to improve upon with our sampling method. Depending on the domain
of context for any given network, certain motifs will be more prevalent than others in terms of the frequency of occurrence. For example, the 
number of recorded instances for each of the 13 motifs is displayed below for a network of North American city reachability by airline travel.

![Motifs Counts](assets/city_motif_counts.png)

Motif counting will ultimately act as the bottleneck in our entire pipeline to process and cluster any given network as the most time-consuming step,
so later on we'll introduce sampling techniques that will obtain a sparser subset of the graph to speed up counting while still providing a fairly 
accurate estimate of the optimal cluster we would obtain with the entire network. But for now, let's move on to discussing the algorithms we've used
to perform spectral clustering based on motif occurrences.

# Spectral Clustering Algorithms

## Algorithm 1

## Algorithm 2

# Network Sampling

# Results 

# Conclusions

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