# Polkadot Node Metrics
This is a sample for polkadot expose metrics and use Prometheus and Grafana
to visualize these metrics.

## Prerequisite
### Install Docker
```
sudo apt-get update

sudo apt-get -y install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

sudo apt-get -y update

sudo apt-get -y install docker-ce
```
### Install Docker-compose
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose
```

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
