## :busts_in_silhouette: Components

This project was made by:
* Mariana Brito Azevedo - Student in Computer Engineering at UFRN
* Thaís de Araújo de Medeiros - Student in Computer Engineering at UFRN

## :mag: About this project

This project aims to carry out an adaptation of the guided project _"Building Fast Queries on a CSV"_ from the course Algorithms Complexity, made by Dataquest.io. Thus, using the dataset _"The Reddit Climate Change Dataset"_, 3 functions were created with two different implementations, in order to compare the performance of each one of them. Those 3 main functions are:

1. Given an id of a message on Reddit, return all information about the message;
2. Given a lower and upper bound of the "sentiment" column, return all messages with sentiment values between the lower and upper bounds;
3. Given a parameter value, return two messages whose sum of the value of the "score" column is equal to the parameter. Return -1 if it doesn't exist.

##### :warning: Important! 

It is important to say that this is a very large dataset, with more than 4.5 million rows (approximately 4GB), so some challenges were faced, like the limit of RAM memory at Google Colaboratory and the runtime of some functions.

## :bulb: About the solution

### Function 1 
This function had to made the following query: __Given an id of a message on Reddit, return all information about the message__.

Two implementations were made. The first one was done by iterating over all the rows of the dataset, while the second was done using the data structure named dictionary.

To compare the performance of both approaches, it was created a list with 100 random ids from de dataset, and was calculated the total time to find those 100 ids in the dataset using both approaches. Doing a time analysis, it was seen that the function implemented with a dictionary was `115.193` times faster than the function implemented with a loop over all rows.

### Function 2 
This function had to made the following query: __Given a lower and upper bound of the "sentiment" column, return all messages with sentiment values between the lower and upper bounds__.

To execute this query, it was implemented one function responsible for performing the binary search, and other function responsible for search all the messages between two values of sentiments. To this query, it was used only one approch, so, it wasn't possible to compare time performance.

### Function 3
This function had to made the following query: __Given a parameter value, return two messages whose sum of the value of the "score" column is equal to the parameter. Return -1 if it doesn't exist__.

Two implementations were made for this query. The first one was done by iterating over all the rows of the dataset (two times) and checking if the sum of the values of those two rows were equal to the target, while the second was done using the data structure named dictionary.

To compare the performance of both approaches, it was created a list with 10000 random values between 0 and 200, and was calculated the total time to find those 10000 values in the dataset using both approaches. Doing a time analysis, it was seen that the function implemented with a dictionary was `1573` times faster than the function implemented with a double loop over all rows.

