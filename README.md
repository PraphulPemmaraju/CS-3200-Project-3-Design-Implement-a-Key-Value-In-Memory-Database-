# CS-3200-Project-3-Design-Implement-a-Key-Value-In-Memory-Database-
Project 3 for CS3200 - Database Design

Tasks
(10 pts) Provide the problem requirements and the conceptual model in UML for your project. You can reuse the one made on previous projects, but describe the functionalities that you selected to be used as an in-memory key-value storage, (e.g. most viewed products, a shopping cart, current logged-in users, etc).
(30 pts) Describe the Redis data structures that you are going to use to implement the functionalities you described in the previous point. (example To implement the most viewed products I will use a Redis sorted set with key "mostViewed:userId", product ids as the values and a score of the number of views of the product.). You can use/describe more than one data structure, you will need to implement at least one.
(30 pts) The redis commands that you would use to interact with your specific Redis structures. 
Example: I will keep a sorted set with the most viewed products in my application. Therefore I need:
Initialize: 
FLUSHALL
Get the list of most viewed items for user duto_guerra: 
ZREVRANGE mostViewed:duto_guerra 0 -1
When user duto_guerra visits produc p1234 one more time:
ZINCRBY mostViewed:duto_guerra 1 p1234
etc...
Describe the commands for all your use cases. Make sure to include all CRUD operations
