# Intro to Kafka

## What's Covered?

- [Intro to Kafka](#intro-to-kafka)
  - [What's Covered?](#whats-covered)
  - [What is Apache Kafka?](#what-is-apache-kafka)
  - [What is an Event Streaming Platform?](#what-is-an-event-streaming-platform)
  - [Kafka Terminology & Client API's](#kafka-terminology--client-apis)
  - [Installation](#installation)
      - [Install 7-Zip](#install-7-zip)
      - [Install Kafka](#install-kafka)

- Building Enterprise Standard Kafka Clients using Spring Boot
  - Build Kafka Clients using Producer and Consumer API

- Resilient Kafka Client applications using Error-Handling/Retry/Recovery

- Writing Unit & Integration tests using JUnit 5

<>

## What is Apache Kafka?
Apache Kafka is used as a Streaming Platform.  In the past, all the applications were built using monolithic architecture.  That means all the functionalities will reside in one single application.
The example here is a retail application and some of the related services are orders, service, payment, service, inventory service and notification service. All those services will reside in one single application and share the same database.

<img>

This kind of architecture was proven to fail under heavy load.  Things have changed as the current state of development uses a more modern architecture, which is the microservices architecture.  As you can see here, the application in itself is decomposed into microservices and each microservice has its own database.

<img>

But as a whole, in order to deliver the business functionality or value, multiple microservices interact with each other using some communication protocol.  The arrows represents the communication between them, but I can definitely say it looks like messy spaghetti.

The expectation of the apps that are built today have a new requirement, which is providing real time notifications and the ability to process events as they occur.  In order to support that, we need to have middleware in between a full blown architecture which looks like this.

<img>

This is a micro service architecture.  The middleware that we are using here is an **Event Streaming Platform**.  At its core, each microservice will have an **Producer API**, which will geenrate events. Other services read those events using a **Consumer API** and take necessary action as the events occur. 

In a nutshell, each micro servers will have an API and it will have an event producer and event consumer.

<br>

## What is an Event Streaming Platform?
And event streaming platform allows the application to produce and consume a stream of records, like a messaging system. The three Principles of an Event Streaming Platform are:

1. Producers and Consumers subscribe to a stream of records
2. Store stream of events
3. Analyze and Process Events as they occur

<br>

## Kafka Terminology & Client API's

| Term      | Description |
| ----------- | ----------- |
| Kafka Cluster   | Consists of multiple brokers at the heart of Kafka  |
| Kafka Broker   | What all the Kafka clients interact with        |
| Apache ZooKeeper   | Manages Brokers by keeping track of their health       |
| Kafka Producers   |  Writes data to the cluster       |
| **Producer API**      | The client uses this API to write data to the cluster      |
| Kafka Consumers   | Entities that read data from the cluster        |
| **Consumer API**   | API used by entities to read data from the cluster       |
| **Connect API**   | Advanced API that Contains Source & Sink Connectors        |
| Source Connector   | Pulls data from an external data source like, DB file system or elastisearch        |
| Sink Connector   | Does the opposite of Source Connector        |
| **Streams API**   | Can take data from Kafka and perform transformations on it and send it back to the cluster        |

<br>

## Installation

#### Install 7-Zip
In order to download Kafka on Windows you will need to download 7-Zip first.  If you're on Mac or Linux, skip to **Install Kafka**.

1. Go to [https://www.7-zip.org/](https://www.7-zip.org/) and click "Download" for "Widnows 64-bit x64"

2. Once the `.exe` has donwloaded, click on it, and allow it to install in the default location which is `C:\Program Files\7-Zip\`. After it installs, close the installer.


#### Install Kafka
1. Google "download apache kafka" and it will take you [here](https://kafka.apache.org/downloads)
> In this demo I've used version **3.1.0**

2. Under **Binary Downloads**, next to Scala 2.13 click `kafka_2.13-3.1.0.tgz`.  This will take you to a new page.

3. Click the link at the top of the page to download under "We suggest the following site for your download:" `https://dlcdn.apache.org/kafka/3.1.0/kafka_2.13-3.1.0.tgz`

4. Open the folder that it downloaded to (most likely "Downloads")



