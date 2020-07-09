# Change Data Capture with Debezium Demos

This demo consists of 3 scenarios that you can use to demonstrate the Change Data Capture (CDC) capabilities of Red Hat Integration with Debezium, Apache Kafka and Apache Camel Kafka Connectors.

### Audience

Developers, Architects, Data Integrators

### Prerequisites

- OpenShift
- Debezium
- AMQ Streams

### Duration

Each basic scenario should be able to be completed in between 10-20 minutes. The advanced scenario depends on the features to demonstrate.

### Provisioning Time

This workshop should be available after 60-75 minutes. It could fortuitously fail in the deployment, please just try again as it could be fixed already. If take more than 3 attempts, please do send an email to raise a ticket to: rhds-help@redhat.com
Relevant information is sent in the final email

## Scenarios

### Introducing Debezium

In this scenario you are capturing events from a mysql database to Apache Kafka. You can go over the data structure of the event for each of the possible changes in the database: create, update and delete. 

This is a basic demo where everything is already set up for you to go over the solution pattern from the solution explorer web application.

### Data Replication

The second scenario covers how to avoid dual writes. You have a legacy PHP application that needs to update an Elasticsearch index with the new orders captured for future search. The CDC part is covered with Debezium connectors and includes the use of Single Message Transformations The second part consists of the deployment of the new Camel Kafka Connectors.

This is a basic demo where everything is already set up for you to go over the solution pattern from the solution explorer web application

### Advanced Demonstrations
The third scenario can be used to demonstrate advanced configurations and requirements for Debezium. 

This is an advanced demo where there are only a base postgresql and mongodb deployments as well as a kafka cluster. You can use it to show how to configure the database for CDC, how to deploy a Kafka Connect cluster using AMQ Streams and how to configure a connector either using the REST API or the OpenShift Custom Resource Definition.
