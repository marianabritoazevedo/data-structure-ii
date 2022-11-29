# Building a network with wikipedia

This project aims to build a network from wikipedia page links, and perform many analyses in this network. For this, the `2022 FIFA World Cup` wikipedia page was used as the initial node of the network.

![Img copa](https://mundoconectado.com.br/uploads/chamadas/copa-2022_2.jpg)

In this way, the network from wikipedia links, starting with `2022 FIFA World Cup` was created and pre-processed, and then, it was analyzed the degree, closeness, betweenness and eigenvector centraility for this network; it was visualized the core and the shell; and finally, it was created a data pipeline for this network, including the steps of collecting data, cleaning data, and export the results of the final artifact.

## Pre-processing the network

The image below shows the process of cleaning data for the creation of this network. Initially, after collecting all the links with only one layer deep, there were 78588 nodes and 212551 edges. Then, two steps of pre-processing were made: eliminate duplicated nodes and eliminate nodes with degree = 1. After these steps, the final network had 27055 nodes and 161018 edges.
