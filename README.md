# Scylla DB
![scylla](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTje3-neQpy-pNS20FM59JtZvSuKBNk7EFKDA&usqp=CAU)
## Abstract
In this paper, There is an introduction to Scylla. First, it start with an overview of the technology and where it stand in the NoSQL world. Then, there are some example use cases and go over some terms that will be useful later.
## Introduction to Scylla DB
**Scylla is an open-source** NoSQL database that enables developers to build mission-critical applications with light speed throughput and ultra-low latency. 
### Overview of the Scylla DB technology
It’s written in C++ and can be used as a drop-in Apache Cassandra replacement. ScyllaDB offers a consistent, high throughput, highly available, and highly scalable NoSQL database. It’s trusted by companies such as IBM, Samsung, CERN, AppNexus, Investing.com, and many others. Apache Cassandra is a great database. One of the top ten most widely used in the world. However, if you use it, you know that it has many problems. So what makes Scylla stand out? There are four major things: lower node count, consistent performance, reduced complexity, and Apache Cassandra compatibility. 

- NoSQL databases, often interpreted as Not Only SQL, provide a mechanism for storage and retrieval of data that is modeled in means other than the tabular relations used in relational databases. The motivations for this approach include simplicity of design, horizontal scaling, and finer control over availability.

- The NoSQL movement started around 2009 and was based on a need for applications that required large amounts of data while maintaining performance and data replication. This replication, typically in global data centers, ensures high availability and tolerance to network partitioning.

**There are different types of NoSQL databases.** One way to classify them is according to their data model. That is, how the logical structure of a database is designed, how the data is connected to each other, and how it is processed and  stored inside the system:

- **Key-Value:** these databases store data in unique key-value pairs. Each key has only one value. Because of the simple data model, querying is fast, and there is no need for a querying language.  Examples include Redis, Aerospike, and RocksDB.

- **Document:** here, data is stored in documents made up of tagged elements. The database assumes the documents encapsulate and encode data in some standard format or encoding. Encodings in use include JSON and XML. Examples are MongoDB and CouchDB.

- **Wide-column store:** these are databases that use columns to store the data. Related columns are grouped into tables, sometimes also known as column families—for example, Apache Cassandra, Apache HBase DynamoDB, and Scylla.

- **Graph:** these databases use nodes and edges to represent and store data. For example, Janus graph and Neo4j. Note that Janus graph can use Scylla as an underlying data store.

Another way to classify NoSQL databases is according to the **CAP theorem**. This theorem claims that in a distributed database system, there can only be two out of the three desirable guarantees: C-A-P, i.e., Consistency, Availability, and Partition Tolerance.

- Consistency guarantees that every read receives the most recent write or an error.

- Availability guarantees that every request receives a non-error response. (Note that here there is no guarantee that the response contains the most recent write)

- Partition Tolerance guarantees that the system continues to operate even when the network drops some messages or there are network failures.

## Use Case of Scylla DB
### The general Scylla use case has the following attributes:

- **Lots of data:** applications dealing with terabytes to petabytes of data.

- **High availability:** applications that require a data store that is always available, typically spread across multiple regional data centers, and that’s used for mission-critical applications.

- **Real-time:** applications that require very fast, sub-millisecond read/write operations.

- **And high performance:** applications that require millions of requests per second per node.

**A few use cases to demonstrate the above:**
1. **Grab:** Grab is a ride-hailing platform that provides on-demand transportation and is a mobile payments leader. They turned to Scylla for metadata storage after their fraud detection system suffered from latency and performance issues. By migrating to Scylla, Grab was able to eliminate the issues they were facing with Redis and Apache Cassandra. That means the team could catch all discrepancies.
![scylla](https://upload.wikimedia.org/wikipedia/en/thumb/1/12/Grab_%28application%29_logo.svg/1200px-Grab_%28application%29_logo.svg.png)

2. **Kiwi.com:** Scylla helps Kiwi fulfill real-time, complex customer requests. The data required to fulfill Kiwi’s customer requests grows exponentially. The team at Kiwi noticed that Apache Cassandra + Redis was too slow and too complicated. One hundred nodes of Apache Cassandra and 50 nodes of Redis were replaced by 21 nodes of Scylla. 
![scylla](https://www.scylladb.com/wp-content/uploads/1024x512-twitter-kiwi.jpg)

3. **IMVU:** IMVU is an online social entertainment company. They migrated from Redis to Scylla to improve performance and scalability. They had over a hundred thousand concurrent users on their 3D avatar social network and were facing issues with scale and performance. IMVU evaluated NoSQL database options. “Scylla beat all the other solutions we tried,” they told us after running the tests. After the migration, the results were better performance, consistently low latencies, major cost savings, high scalability, and reduced administrative complexity.
![scylla](https://cdn.comparably.com/26549036/p/40869_profile_imvu.png)

## Conclusion
**To summarize Scylla DB, these are the main points we covered:**
- It’s a distributed, highly available, high performance, low maintenance, highly scalable NoSQL database.
- In Scylla all nodes are created equal, there are no master/slave nodes.
- Data is automatically distributed and replicated on the cluster according to the replication strategy.
- Scylla supports multiple data centers.
## References
- https://www.scylladb.com/wp-content/uploads/wp-introducing-scylla-cloud.pdf
- https://university.scylladb.com/courses/scylla-essentials-overview/lessons/introduction/topic/nosql-and-scylla/
- https://dev.to/ashraful/introduction-to-scylla-db-342b

