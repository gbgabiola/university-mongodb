# Connecting to Our Class Atlas Cluster from the mongo Shell

## Problem:
When connecting to an Atlas cluster using the shell, why do we provide the hostnames for all nodes when we launch **mongo**? Choose the best answer from the choices below.

## Choose the best answer:
1. So that if the primary node goes down, the shell can connect to other nodes in the cluster instead
2. There really isn't a good reason
3. To make it possible for all the nodes to communicate with each other
4. Because our authentication credentials are not stored on the primary, but on other nodes in our cluster.
5. So that other nodes in the cluster can contact our client, if necessary

## Answer:
5. So that if the primary node goes down, the shell can connect to other nodes in the cluster instead

## Detailed Answer:
The Atlas clusters we've looked at are replica sets. Replica sets are designed so that if the primary node goes down, one of the other nodes will step up to take its place so that clients can continue reading and writing data as if nothing had happened. The mongo shell is one such client.

See the [replication documentation](https://docs.mongodb.com/manual/replication/?_ga=2.40380011.818619118.1525830239-1962173749.1525218334) for more information.