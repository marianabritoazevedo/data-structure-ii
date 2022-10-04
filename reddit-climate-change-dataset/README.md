## :busts_in_silhouette: Components

This project was made by:
* Mariana Brito Azevedo - Student in Computer Engineering at UFRN
* Thaís de Araújo de Medeiros - Student in Computer Engineering at UFRN

## :mag: About this project

This project aims to carry out an adaptation of the guided project _"Building Fast Queries on a CSV"_ from the course Algorithms Complexity, made by Dataquest.io. Thus, using the dataset _"The Reddit Climate Change Dataset"_, 3 functions were created with two different implementations, in order to compare the performance of each one of them. Those 3 main functions are:

1. Given an id of a message on Reddit, return all information about the message;
2. Given a lower and upper bound of the "sentiment" column, return all messages with sentiment values between the lower and upper bounds;
3. Given a parameter value, return two messages whose sum of the value of the "score" column is equal to the parameter. Return -1 if it doesn't exist.

## :bulb: About the solution

### Function 1 
This function had to made the following query: Given an id of a message on Reddit, return all information about the message
Two implementations were made. The first one was done by iterating over all the rows of the dataset, while the second was done using the data structure named dictionary.
