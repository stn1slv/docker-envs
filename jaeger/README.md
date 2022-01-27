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
4. Send several requests to demo-apps to generate traces
```
curl http://127.0.0.1:8080/camel/bookTrip
```
## Jaeger UI
http://localhost:16686/
