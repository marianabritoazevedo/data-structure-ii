# Building a network with wikipedia

This project aims to build a network from wikipedia page links, and perform many analyses in this network. For this, the `2022 FIFA World Cup` wikipedia page was used as the initial node of the network. For this, some python libraries were used to help in this construction, such as the `networkx` and `wikipedia` libraries.

![Img copa](https://mundoconectado.com.br/uploads/chamadas/copa-2022_2.jpg)

In this way, the network from wikipedia links, starting with `2022 FIFA World Cup` was created and pre-processed, and then, it was analyzed the degree, closeness, betweenness and eigenvector centraility for this network; it was visualized the core and the shell; and finally, it was created a data pipeline for this network, including the steps of collecting data, cleaning data, and export the results of the final artifact.

It is important to highlight that this work was carried out in a group. This work was done by me, [Mariana Azevedo](https://github.com/marianabritoazevedo) [![Repository](https://img.shields.io/badge/-Repo-191A1B?style=flat-square&logo=github)](https://github.com/marianabritoazevedo/embedded-ai/tree/main/LeNet-IvaNet),  [Morsinaldo Medeiros](https://github.com/Morsinaldo) [![Repository](https://img.shields.io/badge/-Repo-191A1B?style=flat-square&logo=github)](https://github.com/Morsinaldo/embedded_artificial_intelligence/tree/main/projects/lenet5) and [Thaís Medeiros](https://github.com/thaisaraujo2000?tab=repositories) [![Repository](https://img.shields.io/badge/-Repo-191A1B?style=flat-square&logo=github)](https://github.com/thaisaraujo2000/embedded_artificial_intelligence/tree/main/projects/project_2)

## Pre-processing the network

The image below shows the process of cleaning data for the creation of this network. Initially, after collecting all the links with only one layer deep, there were 78588 nodes and 212551 edges. Then, two steps of pre-processing were made: eliminate duplicated nodes and eliminate nodes with degree = 1. After these steps, the final network had 27055 nodes and 161018 edges.

<p align="center">
  <img src="./img/img1-t3-u2.png">
</p>

## Exploring the network

### Most significant nodes

To visualize the most significant nodes of this network, it was calculated the `indegree` of each degree, which is, the number of connections entering the node, since this is a network directed.

The image below shows the top 10 of these most significant nodes, but it's possible to conclude that most of these nodes refer to past World Cup editions, to soccer-related terms, or even to some prominent teams, including the Brazilian team.

<p align="center">
  <img src="./img/img2-t3-u2.png">
</p>

### Degree, closeness, betweenness and eigenvector centrality

Before checking the results, it is important to understand what these concepts mean:

*  __Degree centrality__: checks the number of connections (neighbors) of a node according to the number of nodes in the network;
*  __Closeness centrality__: checks the average distance of a node to all other nodes. Thus, if the value of this metric is small for a certain node, it means that this node is farther from all other nodes in the network.
*  __Betweenness centrality__: checks the position of a node on the shortest path. That is, if I am analyzing `node i`, among all the shortest paths from `node j` to `node h`, how many of these paths does `node i` form part of?
*  __Eigenvector centrality__: checks the importance of a node based on the importance of its neighbors, that is, it checks whether a given node has important neighbors.

PUT IMAGE

### Centrality distributions

The centrality distributions will be analyzed according to two metrics: degree and closeness centrality, both previously seen in the previous topic.

For this, it is important to understand two important concepts of statistics for read the graphs:

* __PDF__: Probability Density Function. For this case, it will describe that approximately X% of the nodes have degree/closeness centrality equal to Y;
* __CDF__: Cumulative Density Function. For this case, it will describe that approximately X% of the nodes have degree/closeness centrality equal to or less than Y.

__Centrality distribution for degree__

First, the histogram was plotted for the analysis of the data referring to the degree of each node in the network, and as can be seen in the figure below, it appears that most nodes have a step value of less than 250.

<p align="center">
  <img src="./img/histograma-t3-u2.png">
</p>

Then, this histogram was plotted with the PDF and CDF curves, as can be seen in the figure below, and it is possible to see that many nodes have a degree below 100. When checked in the CDF curve, it is inferred that it comes very close to 100% nodes with degree less than 100.

<p align="center">
  <img src="./img/graficos-degree-1.png">
</p>

Thus, in order to try to carry out a more detailed analysis in relation to degree, the network nodes were filtered, so that a subgraph was built only with nodes of degree 100 or higher. It can be noticed that the histogram has already become more distributed, as seen in the plots below, and that approximately 60% of the nodes (among the nodes with degree greater than 100) have a degree in the range of 100-200.

<p align="center">
  <img src="./img/graficos-degree-2.png">
</p>
