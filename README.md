# Polkadot Node Metrics
This is a sample for polkadot expose metrics and use Prometheus and Grafana
to visualize these metrics.

## Run Polkadot Node
detailed docs [How to run a validator on Polkadot](https://wiki.polkadot.network/docs/en/maintain-guides-how-to-validate-polkadot)

## Start Metrics Server
```
docker-compose up -d
```

## Visualized Dashboard
- Grafana UI: http://localhost:3000
- Prometheus UI: http://localhost:9090
- Alertmanager UI: http://localhost:9093

![metrics](https://grafana.com/api/dashboards/12425/images/8296/image)

![metrics](https://grafana.com/api/dashboards/12425/images/8297/image)

## Testing Alert Rules
```
docker exec -it prometheus sh

promtool test rules /etc/prometheus/rules/alerting-rule-tests.yaml
```
