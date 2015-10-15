![MongoDB logo](pics/mongodb-logo-rgb.jpeg)

# MongoDB

This is meant to be a notes document for the area of MongoDB, where most of the material is initially from the course held with <a href="https://university.mongodb.com/courses/M101JS/about">University.mongoDB.com</a>. Youtube clips are accessible for people with a key and are linked as often as possible in this document.

## List of contents
1. [Chapter 1](#chapter_1)
2. [Chapter 2](#chapter_2)

## <a name="chapter_1"></a>Chapter 1
### What is MongoDB <a href="https://www.youtube.com/watch?v=Lfl8hdQOi6Y">»</a>
* Non-relational database
* Stores JSON documents
	* ex. ``{"name":"Andrew"} <- {key:value}``
	* ex. ``{”a”:4, ”b”:2, ”c”:[”ab”, ”ca”, ”cd"]} <- {key:value}``
	* These may have an inner hierarchy as the 2nd example.
* It is schemaless

**What is schemaless?**

* It means that two documents don't need to have the same schema.
* ex. ``one document: {a:5, b:4}, another: {a:5, b:4, c:1}``

**What is/isn't mongoDB?** <a href="https://www.youtube.com/watch?v=-KIC1LXxcGM">»</a>

* IS(document-oriented, is schemaless/has dynamic schema)
* NOT(support joins, support SQL)

The point is that, unlike in a relational database, you are not constrained to follow any particular schema. If you wish to change your schema, you are free to do any of the following:

Begin inserting documents with the new schema.
Perform a bulk update on the existing documents.
Begin updating old documents to the new schema one by one at an appropriate event (such as getting read from or written to), as coded in the application.
Contrast this with what happens in a relational database, where the table must typically be taken offline in order to add columns.

As for the other two answers, MongoDB does not support joins as a design decision because they do not scale horizontally, and it does not support SQL because that query language was built around joins and transactions, and tends to assume table structure rather than the flexible document orientation that MongoDB provides.

### Building an app with mongoDB

Relevant elements <a href="https://www.youtube.com/watch?v=_e0J06elxb8">»</a>

* MongoD process - database server itself
* Mongo Shell - lets you interact with mongoD
* HTTP server - running python, bottle, pymongo within it.
* Client

![Relevant elements](pics/relevant_elements.png)

#### Mongo Shell

**Last lecture <a target="_blank" href="https://university.mongodb.com/courses/MongoDB/M101P/2015_October/courseware/Chapter_1_Introduction/52546afae2d4231cc6083fd8">»</a>**








