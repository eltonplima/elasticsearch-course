## Logstash

Data process pipeline and sends to the elasticsearch or others destinations like kafka topic, http request etc...

* Input => Filter => Output

Each step uses a plugin to handle the data.

> Input and output can use a lot of different plugins like kafka for example
> Filter can do something like find the geographic location of an IP, looking for data on SGDB, etc...
