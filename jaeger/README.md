# Jaeger details
## Streaming deployment strategy
1. Start infrastructure
```
docker-compose -f compose.yml -f kafka/compose-cp.yml -f elasticsearch/compose.yml up
```
2. Start Jaeger components
```
docker-compose -f compose.yml -f jaeger/streaming.yml up

```
3. Start demo-apps
```
docker-compose -f compose.yml -f demo-apps/compose.yml up
```
## Jaeger UI
http://localhost:16686/