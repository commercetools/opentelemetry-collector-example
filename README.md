# OpenTelemetry Collector Example

This folder contains a preconfigured docker compose file for local experiments
with OpenTelemetry. It includes a OpenTelemetry collector, a Jaeger UI, Prometheus, Grafana, and
NewRelic as export target.

To start it use the following command:

```bash
docker-compose --env-file .env up --no-build
```

## NewRelic
The collector is preconfigured to export metric, traces and log entries to NewRelic.
In order to activate it add your NewRelic api key to the `.env` file. Make sure OpenTelemetry Collector service 
in [docker-compose.yml](./docker-compose.yaml) has the NewRelic command uncommented.
Restart the containers.

## Dynatrace
The collector is preconfigured to export metric, traces and log entries to Dynatrace.
In order to activate it add your Dynatrace OTLP endpoint and Dynatrace API key to the `.env` file.
Make sure OpenTelemetry Collector service 
in [docker-compose.yml](./docker-compose.yaml) has the Dynatrace command uncommented.
Restart the containers.

## Jaeger UI

http://localhost:16686

## Grafana

http://localhost:3000

## Prometheus

http://localhost:9090
