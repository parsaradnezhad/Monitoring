## Prometheus and Grafana

<img src="https://kjanshair.blob.core.windows.net/docker/prometheus-introduction/2.png">

### Prometheus :
Prometheus is an open-source monitoring tool that is used to record real-time metrics in a time-series database.
A metric is uniquely identified by its name and set of labels.

```
   metric name               labels                 timestamp     value
┌────────┴───────┐  ┌───────────┴───────────┐    ┌──────┴──────┐  ┌─┴─┐
http_requests_total{status="200", method="GET"}  @1557331801.111  42236
```

Each application or system being monitored must expose metrics in the format above, either through code instrumentation or Prometheus exporters.

#### Prometheus Exporters :
Exporters are libraries that help with exporting metrics from third-party systems as Prometheus metrics.

Multiple exporters can run on a monitored host to export local metrics.

### Grafana:
Grafana is a tool for data visualization, monitoring, and analysis. It is used to create dashboards with panels representing specific metrics over a set period of time

### Usage :
We can use this tools togheter to set up monitoring server
  1. Gathering information with Prometheus
  2. Visualize information with Grafana

### Benefits :
  - Prometheus :
    1. Prometheus is TSDB (Time Series Data Base) :
        - Time series data are simply measurements or events that are tracked, monitored, down sampled and aggregated over time.
    2. Prometheus is Pull based tool :
        - Prometheus actively scrape targets in order to retrieve metrics from them. 
    3. Centralised control :
        - A pull based system enables a rate control with the flexibility of having multiple scrap configurations, thus multiple rates for different targets.
    4. In built Alerting facility :
        - Prometheus pushes alerts to the Alert manager via custom rules defined in configuration files.
    5. Easy for monitoring teams :
        - it’s easy to create Alert rules / conditions in Alert Manager.They can easy configure different endpoints for alerting.
    6. Data visualisation :
        - You can visualize your time series directly in Prometheus Web UI but This GUI is not that much good like Grafana.
    7. Service discovery :
        - Prometheus can discover your targets dynamically and automatically scrap new targets on demand.
    8. Scalability :
        - Prometheus is highly scalable. You can club different Prometheus servers to a single one using federation approach.
    9. PromQL :
        - Prometheus provides a functional query language called PromQL (Prometheus Query Language) that lets the user select and aggregate time series data in real time.
  - Grafana :
    1. Dashboard templating :
        - Dashboard templating helps you to build dashboards that can be reused for different purposes and shared among your organization’s teams.
    2. Provisioning :
        - Grafana allows you to script anything and get control of a large number of dashboards.
    3. Annotations :
        - In Grafana, this feature appears as a graph marker and is useful for correlating data in case something goes wrong.    
    5. Custom plugins :
        - You can use plugins to extend Grafana and integrate it with other software, visualizations, and more.
    6. Alerting and alert hooks :
        - If an anticipated scenario occurs, alerts are activated like tripwires. These events can be reported to the monitoring team through Slack or some other communication channel.
    8. SQL data sources :
        - Grafana’s native SQL support allows you to turn anything in a SQL database into metric data that you can graph. 
    9. Authentication :
        - Grafana supports a variety of authentication styles, including LDAP and OAuth, and lets you map users to organizations.
