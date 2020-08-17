# Logstash

Data process pipeline and sends to the elasticsearch or others destinations like kafka topic, http request etc...

* Input => Filter => Output

Each step uses a plugin to handle the data.

> Input and output can use a lot of different plugins like kafka for example
> Filter can do something like find the geographic location of an IP, looking for data on SGDB, etc...

## Queries and operations via HTTP request

```bash
# Check cluster health
http "http://localhost:9200/_cluster/health?pretty"

# Check nodes information
http "http://localhost:9200/_cat/nodes?v&pretty"

# Create index
http PUT "http://localhost:9200/<INDEX_NAME>"

# Create an index with custom shards and replicas
http PUT http://localhost:9200/<INDEX_NAME>
< """{
  "settings": {
    "number_of_replicas": 2,
    "number_of_shards": 2
  }
}"""

# Check indices
http "http://localhost:9200/_cat/indices?v"

# Delete index
http DELETE "http://localhost:9200/<INDEX_NAME>"
```
