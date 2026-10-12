# EC2 Monitoring Using Prometheus and Grafana

## Project Overview

This project demonstrates infrastructure monitoring on an Amazon EC2 instance using Prometheus and Grafana. It visualizes system metrics and uses threshold-based alerts with email notifications to identify potential performance issues.

## Objectives

- Monitor EC2 system resource utilization.
- Visualize metrics through Grafana dashboards.
- Configure CPU utilization alerts.
- Receive email notifications when alert conditions are met.
- Understand alert recovery and monitoring practices.

## Tools and Technologies

- Amazon EC2
- Prometheus
- Grafana
- Node Exporter
- PromQL
- Email notifications

## Architecture

1. Node Exporter exposes system metrics from the EC2 instance.
2. Prometheus collects metrics from the configured target.
3. Grafana queries Prometheus and displays the metrics in dashboards.
4. A CPU alert rule evaluates utilization against the configured threshold.
5. Grafana sends email notifications when the alert fires and resolves.

## Monitoring and Alerting

The Grafana dashboard displays CPU utilization, memory usage, disk usage, and network traffic.

A CPU alert was configured to trigger when utilization exceeded 80% for five continuous minutes. During testing, CPU utilization reached 92.9%, and an alert notification was received. After utilization decreased to 14.7%, the alert returned to the Normal state and a resolution notification was received.

## Key Learning Outcomes

- Configuring Prometheus as a Grafana data source.
- Visualizing infrastructure metrics.
- Creating threshold-based alert rules.
- Configuring email notifications.
- Understanding alert firing and resolution states.

## Screenshots

Screenshots of the monitoring dashboard, CPU utilization, alert rule, firing notification, and resolved notification are available in the `screenshots/` directory.

## Conclusion

This project demonstrates how Prometheus and Grafana can monitor EC2 system performance, detect high CPU utilization, and notify administrators of alert conditions to support faster troubleshooting and reduce potential downtime.
