# Change data capture with Debezium demos

## Introduction

This demo consists of a set of scenarios that you can use to demonstrate the change data capture (CDC) capabilities of Red Hat Integration with Debezium, Apache Kafka, and Apache Camel Kafka Connectors.

### Audience

- Developers
- Architects
- Data Integrators

### Products and projects

- Red Hat OpenShift
- Red Hat Integration
  - Debezium
  - AMQ Streams
- Apache Camel Kafka Connectors

### Duration

The basic scenarios can be completed in 25 - 30 minutes. The time to complete the advanced scenario depends on the features that you want to try.

## Deployment

To deploy the demos, request the **Change Data Capture with Debezium** workshop from the [Red Hat Product Demo System (RHPDS)](https://rhpds.redhat.com).

### Provisioning time

Workshop provisioning takes 60 - 75 minutes. 

If the workshop fails to deploy, resubmit your provisioning request. If deployment continues to fail after three attempts, open a ticket by sending a message to rhds-help@redhat.com.

After your provisioning request is received, the _Red Hat Product Demo System_ sends you a series of email messages with updates about the status of the request. When your deployment is ready for use, you receive a final email that includes information about how to access the environment. 

## Scenarios

### Introduction to Debezium

In this introductory scenario, you use Debezium to capture data change events from a MySQL database and send change event records to Apache Kafka. You can go over the data structure for each type of event record: creates, updates, and deletes. 

This is a basic demo where everything is already set up for you to go over the solution pattern from the Solution Explorer web application.

#### Video

### Data replication

The data replication scenario demonstrates how to use Debezium to avoid dual writes. In the scenario, you have a legacy enterprise application built on PHP, that sends orders and records into a database. To enable faster querying of your orders, you want to  send the records for each new order event to an Elasticsearch index. 

The scenario makes use of Debezium connectors and Single Message Transformations (SMTs). The second part of the demo introduces the new Camel Kafka Connectors.

The components used in this scenario are deployed in the Solution Explorer, and are ready for you to use.

#### Video

[![](https://i.ytimg.com/vi/LVizd46AD_Q/hqdefault.jpg?sqp=-oaymwEZCPYBEIoBSFXyq4qpAwsIARUAAIhCGAFwAQ==&rs=AOn4CLCLbGoabBwtHlxtWbdL9slZ0I-Oug)](https://www.youtube.com/watch?v=LVizd46AD_Q)

### Advanced demonstrations

Use the advanced demo to explore advanced configurations and requirements for Debezium. 
To access the environment for the advanced demo, use the **debezium-advanced-demo** OpenShift project. 
The **debezium-advanced-demo** project has the following components deployed:

- A base PostgreSQL database
<!-- - A MongoDB database !-->
- A Kafka cluster

The advanced demonstration does not follow a set script. You can use the components that are available in the project in any way that you want. For example, try the following tasks:

- Deploy a Kafka Connect cluster using AMQ Streams.
- Deploy and configure a Debezium connector for PostgreSQL and you it to send data from the database to Kafka.
- Configure the connectors by using the REST API, or by using OpenShift Custom Resource Definitions (CRDs).

#### Video

### Support and ownership
If you have any questions or are in need of support, reach out to [Hugo Guerrero](https://github.com/hguerrero).
