Project for trying out prometheus. 

Start with `docker-compose up`.
- Prometheus: http://localhost:9090
- Grafana: http://localhost:8080
- Web app with metrics: http://localhost:3000

## Grafana
Grafana can connect to prometheus on url `http://prometheus:9090`


## PromQL
Query for getting error percentage for web app:
`sum by (path) (api_request_total{code=~"5.*"}) / sum by (path) (api_request_total)`

Use in combination with visualization in kibana, e.g. Stat.