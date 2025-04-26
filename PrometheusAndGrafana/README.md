#Monitoring with Prometheus and Grafana
This project sets up a monitoring stack using Prometheus and Grafana to collect and visualize system metrics.

Node Exporter is used to collect system-level metrics, such as CPU usage, memory, disk, and network stats. These metrics are exposed on a specific port (9100), which Prometheus scrapes at regular intervals. Prometheus itself serves as the data collection and storage layer, scraping metrics from Node Exporter and storing them for visualization.

Grafana is then used to visualize the collected metrics. After adding Prometheus as a data source in Grafana, you can import a pre-configured dashboard to display a variety of system metrics. This provides a comprehensive view of system performance, which is useful for monitoring and troubleshooting.

To run the stack, you configure a docker-compose.yml file to launch Prometheus and Grafana containers, along with a prometheus.yml file to define how Prometheus scrapes metrics from Node Exporter. Once the services are up and running, you can access Prometheus on localhost:9090 for monitoring, and Grafana on localhost:3000 for visualizing the data.

