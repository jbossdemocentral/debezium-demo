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
- Apache Camel Kafka Connect Connectors

### Duration

The basic scenarios can be completed in 25 - 30 minutes. The time to complete the advanced scenario depends on the features that you want to try.

## Deployment

To deploy the demos, request the **Change Data Capture with Debezium** workshop from the [Red Hat Product Demo System (RHPDS)](https://rhpds.redhat.com).

### Provisioning time

Workshop provisioning takes 60 - 75 minutes. 

If the workshop fails to deploy, resubmit your provisioning request. If deployment continues to fail after three attempts, open a ticket by sending a message to rhds-help@redhat.com.

After your provisioning request is received, the _Red Hat Product Demo System_ sends you a series of email messages with updates about the status of the request. When your environment is ready to use, you receive a final email that includes information about how to access the environment. 

## Scenarios

### Introduction to Debezium

In this introductory workshop, you use Debezium to capture data change events from a MySQL database and send change event records to Apache Kafka. 
After you complete the tasks in the workshop, you'll have a better understanding of the data structures that Debezium uses as it sends event records to Kafka for standard database operations (`CREATE`, `UPDATE`, and `DELETE`). 

The provisioning process for the workshop deploys the components that are used in this scenario into the **debezium-basic-demo** namespace.
Follow the _Introducing Debezium_ script in the Solution Explorer for guidance in completing the tasks for this demo.

#### Video

### Data replication

The data replication scenario demonstrates how you can use Debezium to send data from your application database to another system without performing _dual writes_, that is, without making the application responsible for writing the data to two separate systems. In the scenario, a legacy enterprise application, built on PHP, sends orders and records into a database. To enable faster querying of your orders, you want to send the records for each new order event to an Elasticsearch index. 

The scenario makes use of Debezium connectors and Single Message Transformations (SMTs). The second part of the demo introduces the new Apache Camel Kafka Connect Connectors.

The components that are used in this scenario are deployed into the **debezium-complete-demo** namespace. 
Follow the _Data Replication_ script in the Solution Explorer for guidance in completing the demo tasks.

#### Video

[![](https://i.ytimg.com/vi/LVizd46AD_Q/hqdefault.jpg?sqp=-oaymwEZCPYBEIoBSFXyq4qpAwsIARUAAIhCGAFwAQ==&rs=AOn4CLCLbGoabBwtHlxtWbdL9slZ0I-Oug)](https://www.youtube.com/watch?v=LVizd46AD_Q)

### Advanced demonstrations

Use the advanced demo to explore advanced configurations and requirements for Debezium. 
To access the environment for the advanced demo, use the **debezium-advanced-demo** OpenShift project. 
The following components are deployed to the **debezium-advanced-demo** namespace:

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
