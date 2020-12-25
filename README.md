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
- grafana UI: http://127.0.0.1:3000
  default user: admin/admin
- prometheus UI: http://localhost:9090/targets

![metrics](https://grafana.com/api/dashboards/12425/images/8296/image)

![metrics](https://grafana.com/api/dashboards/12425/images/8297/image)
