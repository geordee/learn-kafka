# Elasticsearch

## Install

See https://www.elastic.co/guide/en/elasticsearch/reference/8.5/targz.html

## Configuration

Simple (insecure) configuration for local development.

```bash
vi /usr/local/elasticsearch/config/elasticsearch.yml
```

> elasticsearch.yml

```yaml
# Enable security features
xpack.security.enabled: false

xpack.security.enrollment.enabled: false

# Enable encryption for HTTP API client connections, such as Kibana, Logstash, and Agents
xpack.security.http.ssl:
  enabled: false

# Enable encryption and mutual authentication between cluster nodes
xpack.security.transport.ssl:
  enabled: false
```
