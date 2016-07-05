# dist_trans :globe_with_meridians:

A flexible set of tools, algorithms, and data structures for building reliable
distributed systems.

* fault injection
* replication: (broadcast, chain) x (async, quorum)
* consensus
* fifo messaging
* replicated KV
* distributed transactions
* eventual consistency
* leadership election, detection
* chain ordering
* membership
* failure detection
* gossip

This library is built around the concept of the "asynchronous network" where
systems communicate using messages that may be arbitrarily delayed or lost
in-transit. We extensively test our implementations using a simulator that
delays and drops messages between components, to ensure that various
correctness invariants hold in the presence of failures. Periodic functionality
is rapidly exercised with the help of generic clocks. This simulator may be used
independently for building robust distributed systems.

## Use Cases

1. engineer wants to create riak
1. operator wants to swap out existing leader of replicated log
1. operator wants to add active slave
1. engineer wants to create cockroach
1. operator wants to add replica to dynamo style kv
1. engineer wants to create kafka
1. operator wants to remove load balancer
1. operator wants to view traffic statistics
1. engineer wants to create redis cluster
1. operator wants to trace rpcs
1. engineer wants to create actordb
1. operator wants to migrate kv across datacenters
1. operator wants to add replicas in other datacenter
1. operator wants to add read slaves in other datacenter
1. operator wants to modify datacenter failover policy
1. engineer wants to create mcrouter
1. engineer wants to create ceph
1. engineer wants to create hdfs
1. engineer wants to create maprfs
