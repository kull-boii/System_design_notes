# Consensus in distributed systems
A group of computer nodes that act as a single entity

in reality these system components are never perfect, they are prone to hardware failures, packet drops, slow network, clock skews etc

these components should agree on some data value that is needed during computation to act as a single entity

## Scenarios that require consensus
eg. distributed database where the data is replicated to all nodes 
- ordering of updates
- detection of suspected failures 
- leader election process
- exclusive access to a resource


## Consensus Algorithms
- Apache Zookeeper
- RAFT (Hashicorp)
- PAXOS (Google's chubby)
