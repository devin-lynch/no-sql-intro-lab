![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)

# NoSQL Research Lab

## Explainer

Up until now in the cohort we have stored data only in what are known as relational databases (SQL is the most well known type of relational DB querying language). Relational databases structure our data into tables. Today we will learn about a different type of database: a non-relational one. 

## Lab

In this lab you will be researching, either individually or in groups, answer to the following questions about noSQL databases. The intention is for you to spend some time learning about the fundamental differences between the type of databases we have seen before and the new type we will be learning about today. Even more importantly, you will learn about why two types of databases are used, and what situations fit each type of db. 

## Setup

Fork and clone this repository and answer questions as you research directly in the README. You do not have to submit this lab, but you will want to have it on hand for reference in the future. 

## Questions:

1. What does the term noSQL refer to, and what other term is often used synonymously with noSQL?
* 'Not only SQL' a non-relational database that store data differently from relational tables. 
* It uses documents instead of tables.
* Does not use rows/columns
* Can be both tabular and non-tabular

1. What are some of the common arguments for using a non-relational versus a relational db?
* Greater scalability (in terms of changing data structure)
* Personal preference
* Don't have to worry about avoiding data duplication (due to lowered storage costs)
* Optimized for developer productivity
* Allows devs to store huge amounts of unstructured data, giving more flexibility to adapt to changes

1. In this class we will be using the document style of non-relational databases. What are the charecteristics of a document based db? 
* Store data in documents similar to JSON (JavaScript Object Notation) objects. 
* Key/value pairs -- values are a variety of supported types
* Allows for the data model to evolve vs having a rigorous structure
* No enforced schema

1. In this class we will be using Mongo specificially as our no-SQL db. Look into Mongo and answer this question: what is the primary difference between how Mongo is maintained vs SQL?
* Mongo is more advanced and capable of handling big data with dynamic schema features. MongoDB is used to save unstructured data in JSON format.
* MongoDB is open source, made by a smaller company. One implementation to rule them all with Mongo. One team makes all of the Mongo tools. Tight integration of all mongo features. 
* Some versions of SQL are closed source (Oracle, MySQL, Microsoft SQL Server), though some versions are open source (PostgreSQL, SQLite)

1. Mongo DBs are organized into documents. Describe an example of a table in SQL that contains users, and then describe the equivalent DB setup in Mongo. 
* user -> blog (in SQL use etiher FK or join)
* Mongo woul dhave embedded objects or 'sub documents'
  * { userName, email, blogs: [{ blog }, { blog }] }

1. What is an example situation where a Mongo database makes sense versus a non-relational db?
* Fast paced development when the data models might change frequently
* Adding features to the database
* Situations that involve collaborations between lots of teams

1. What are the benefits of SQL databases? NoSQL Databases?
* SQL benefits: 
  * Vertical scaling (scale-up with a larger server) 
  * Multi-record ACID transactions are supported
  * Commonality of language, lack of complex code
  * Established an used many places
* NoSQL benefits:
  * Familiar languages to devs
  * 'data that is accessed together should be stored together'
  * Flexible data models
  * Horizontal scaling 
  * Fast queries, easy for developers

1. Explain the differences between ACID and BASE models.
* ACID:
  * Atomic (Each transaction is either properly carried out or the process halts and the database reverts back to the state before the transaction started. This ensures that all data in the database is valid.)
  * Consistent (A processed transaction will never endanger the structural integrity of the database.)
  * Isolated (Transactions cannot compromise the integrity of other transactions by interacting with them while they are still in progress.)
  * Durable (The data related to the completed transaction will persist even in the cases of network or power outages. If a transaction fails, it will not impact the manipulated data.)
* BASE:
  * Basically Available (Rather than enforcing immediate consistency, BASE-modelled NoSQL databases will ensure availability of data by spreading and replicating it across the nodes of the database cluster.)
  * Soft State (Due to the lack of immediate consistency, data values may change over time. The BASE model breaks off with the concept of a database which enforces its own consistency, delegating that responsibility to developers.)
  * Eventually Consistent (The fact that BASE does not enforce immediate consistency does not mean that it never achieves it. However, until it does, data reads are still possible (even though they might not reflect the reality)

1. What should you consider when deciding between using a relational database or a non-relational database for your project?
* Personal preference
* Scale of traffic
* Speed
* What kind of flexibility will you 

## Visual Comparisons

### Structure

![](https://media.git.generalassemb.ly/user/16103/files/65db7f00-afd5-11ea-926a-e51b2fd2be08)

### Relationships

![](https://media.git.generalassemb.ly/user/16103/files/5eb47100-afd5-11ea-8cae-0a65c924be4b)

### Use Cases

![](https://media.git.generalassemb.ly/user/16103/files/7f7cc680-afd5-11ea-82c8-10ed74ee2222)

## Additional Readings

Pick an additional reading to go through with a classmate. Reflect on how the
article changes the discussion. What have you learned?

  _**Note:** You do not have to read about the different types of SQL and NoSQL. We will use PostgreSQL and MongoDB in this course._
- [ACID vs. BASE Explained](https://neo4j.com/blog/acid-vs-base-consistency-models-explained/)
- [PostgreSQL Use Cases](https://www.cybertec-postgresql.com/en/postgresql-overview/solutions-who-uses-postgresql/)
- [MongoDB Use Cases](https://www.mongodb.com/use-cases)
- [What the heck are you actually using NoSQL for?](http://highscalability.com/blog/2010/12/6/what-the-heck-are-you-actually-using-nosql-for.html)
- [A co-Relational Model of Data for Large Shared Data Banks](http://queue.acm.org/detail.cfm?id=1961297&repost)
- [A brief history of databases](http://avant.org/media/history-of-databases)
- [NoSQL Databases: An Overview | ThoughtWorks](http://www.thoughtworks.com/insights/blog/nosql-databases-overview)
- [When to choose CouchDB vs RDBMS?](http://stackoverflow.com/a/2731207/402618)
- [CAP Twelve Years Later: How the "Rules" Have Changed](http://www.infoq.com/articles/cap-twelve-years-later-how-the-rules-have-changed)
