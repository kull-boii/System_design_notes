# Multi-master replication

Multi-master replication is a method of database replication which allows data to be stored by a group of computers, and updated by any member of the group.

All members are responsive to client data queries. 
basically multiple masters.

The multi-master replication system is responsible for propagating the data modifications made by each member to the rest of the group and resolving any conflicts that might arise between concurrent changes made by different members.

this help us achieve availability and fault tolerance but we have to compromise on consistency 

communication and replication in Multi-master systems are handled via a type of Consensus algorithm

to learn more about what consensus algorithm is and how it helps to manage multiple clusters, checkout consensus.md

## Additional Resource:
- [internals of Aurora Multi-Master for the MySQL-compatible edition of Aurora](https://aws.amazon.com/blogs/database/building-highly-available-mysql-applications-using-amazon-aurora-mmsr/)
