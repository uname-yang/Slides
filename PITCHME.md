# DataDog 101

#HSLIDE

## 1 Overview

- Dashboards
- Infrastructure
- Monitors
- Metrics
- Integrations
- APM

#HSLIDE

### example: quick look

#HSLIDE

![event](images/01_event.png)

#HSLIDE

![dashboard](images/02_dashboard.png)

#HSLIDE

![dashboard](images/03_timeboard.png)

#HSLIDE

![dashboard](images/04_sreenboard.png)

#HSLIDE

![05_hostmap](images/05_hostmap.png)

#HSLIDE

![06_monitor](images/06_monitor.png)

#HSLIDE

![07_metrics](images/07_metrics.png)

#HSLIDE

![08_integration](images/08_integration.png)

#HSLIDE

![09_apm](images/09_apm.png)

#HSLIDE

## 2 Collection

> Getting Metrics and Events into Datadog

#HSLIDE

### Integrations

1. Integrations with [AWS,Gitlab ...]
2. Integrations with [Mysql,Nginx ...]
3. Notification Integrations [Slack,Webhooks ...]
4. Frameworks, Libraries, Trace [Python,Java ...]

- <https://docs.datadoghq.com/integrations/amazon_web_services>
- <https://docs.datadoghq.com/integrations/amazon_ecs/>
- <https://docs.datadoghq.com/integrations/mysql/>
- <https://docs.datadoghq.com/tracing/setup/>

#HSLIDE

### Tracing Java Applications

#HSLIDE

#### Install the Agent

> <https://docs.datadoghq.com/getting_started/agent/>

The Datadog Agent is software that runs on your hosts. It collects events and metrics from hosts and sends them to Datadog, where you can analyze your monitoring and performance data.

![agent_install](images/10_agent_install.png)

#HSLIDE

#### Instrument Java Applications

> <https://docs.datadoghq.com/tracing/setup/java/>

![instrument](images/11_instrument_application.png)

```bash
wget -O dd-java-agent.jar 'https://repository.sonatype.org/service/local/artifact/maven/redirect?r=central-proxy&g=com.datadoghq&a=dd-java-agent&v=LATEST'
```

Finally, add the following JVM argument when starting your application in your IDE, Maven or Gradle application script, or java -jar command:

```bash
export DD_SERVICE_NAME=cdf-retrieval-ocs-205065-sharedservices
export DD_AGENT_HOST=localhost
export DD_TRACE_AGENT_PORT=8126
export DD_TRACE_GLOBAL_TAGS=env:local,keyword:cdf

java -javaagent:<DD-JAVA-AGENT-PATH>.jar \
     -Ddd.agent.host=$DD_AGENT_HOST \
     -Ddd.agent.port=$DD_TRACE_AGENT_PORT \
     -jar <YOUR_APPLICATION_PATH>.jar
```

#HSLIDE

### Tags

> <https://docs.datadoghq.com/getting_started/tagging/>

#HSLIDE

#### example: tags on metrics

#HSLIDE

### Agent Architecture

- <https://github.com/DataDog/dd-agent/wiki>

![agent_architecture](images/12_agent_architecture.png)

#HSLIDE

## 3 Dashboard

> Using data you have collected

> example: Dashboard

#HSLIDE

## 4 Monitors: Notifications and Alarm

> Monitors can also be thought of as alerts nand notifications.

> example: Monitors

#HSLIDE

## 5 docs and tickets

- <https://docs.datadoghq.com/>
- <https://app.datadoghq.com/help>
