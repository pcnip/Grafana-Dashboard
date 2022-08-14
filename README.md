# Grafana Dashboard for Polkadot and Kusama node
Displays metrics collected from Polkadot instance and Prometheus node_exporter (exporter for hardware and OS metrics).

1. Add two jobs `substrate_node` and `node_exporter` to `prometheus.yml`:
```
    - job_name: "substrate_node"
    scrape_interval: 5s
    static_configs:
      - targets: ["localhost:9615"]
  - job_name: "node_exporter"
    scrape_interval: 5s
    static_configs:
      - targets: ["localhost:9100"]

```
2. Import json file: Grafana > Dashboards > Import > Upload JSON file, select Prometheus datasource and then click "Import"
3. Select Chain Metrics "Substrate" and Chain Instance Host "localhost:9615"

![screenshot](https://github.com/pcnip/Grafana-Polkadot-Dashboard/blob/main/Dashboard_Screenshot.jpg?raw=true)
