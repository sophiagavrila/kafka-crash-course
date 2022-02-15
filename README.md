# Intro to Kafka

## What's Covered?
- Intro to Kafka
  - [What is Kafka?](#what-is-apache-kafka)
  - [What is an Event Streaming Platform?](#what-is-an-event-streaming-platform)

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

## Traditional Messaging System vs Kafka Streaming Platform


## Kafka Terminology & Client API's

| Term      | Description |
| ----------- | ----------- |
| Producer API      | Title       |
| Kafka Producers   | Text        |
| Consumer API   | Text        |
| Kafka Consumers   | Text        |
| Streams API   | Text        |
| Kafka Streams   | Text        |
| Connect API   | Text        |
| Source Connector   | Text        |
| Sink Connector   | Text        |
| Kafka Broker   | Text        |
| Kafka Cluster   | Text        |
| Apache ZooKeeper   | Text        |