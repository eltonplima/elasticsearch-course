## Roles

### Primary node
node.master

### Data node
node.data

### Ingest node
node.ingest

### ML node
node.ml
xpack.ml.enabled

### Coordination node

Coordination refers to the distribution of queries and the aggregation of results

> Useful for large clusters

node.master:false
node.data:false
node.ingest:false
node.ml:false
xpack.ml.enabled:false

### Voting node

node.voting_only:true|false

> Useful for large clusters
