## Question 4

Create a simulated scenario, where you want to take a trip with the following route:

*   City 1 (North) to city 2 (South)
*   City 2 (South) to city 3 (Northeast)
*   City 3 (Northeast) to city 4 (Central-West)
*   City 4 (Central-West) to city 5 (Southeast)

#### Solution

To create this simulated scenario, five cities were chosen, one from each region of Brazil, and they were related to their respective airports through the creation of a dictionary. Below are the cities and airports chosen for each Brazilian region:

Region       | Airport | City
:--------:   | :------:| :--------:
North        | SNNG    | Novo Progresso
Northeast    | SBIL    | Ilhéus
South        | SSCN    | Canela
Southeast    | SBRP    | Ribeirão Preto
Central-West | SBAN    | Anápolis

Then, for each path, functions `shortest_path` and `shortest_path_length` from `nxviz` library were used to calculate the shortest path and its length, respectively. Below, it's possible to check the image with the complete route taken from city 1 to city 5, whose route size is 7, and then the route taken in each path of the complete route is verified.

![img](./img/img-q4-t2-u2.png)

Table with each path:

Path                                           | Path length 
:-------------------------------------------- | :------:
City1 (Novo Progresso) -> City2 (Canela)       | 3   
City2 (Canela) -> City3 (Ilhéus)               | 2   
City3 (Ilhéus) -> City4 (Anápolis)             | 1    
City4 (Anápolis) -> City5 (Ribeirão Preto)     | 1    
