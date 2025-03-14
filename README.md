# Project Brown Fox

The well-known phrase 'a quick brown fox jumps over the lazy dog' exercises every letter of the alphabet. In the late 19th century, the sentence was used as typing practice.

The goal of Project Brown Fox is to define a simple but comprehensive system architecture that features many common components of modern web services. This common design can then be implemented across several languages and frameworks to demonstrate the benefits of each.

## Frontent

A UI service should exist for each supported language that provides an interface to each backend API.

### Framework Support

| Framework       | REST    | GraphQL | Websocket | WorkerService | Tests   |
| --------------- | ------- | ------- | --------- | ------------- | ------- |
| Angular         | &cross; | &cross; | &cross;   | &cross;       | &cross; |
| Python (flask)  | &cross; | &cross; | &cross;   | &cross;       | &cross; |
| React           | &cross; | &cross; | &cross;   | &cross;       | &cross; |
| Vue             | &cross; | &cross; | &cross;   | &cross;       | &cross; |


## Backend

### Features

#### Microservice Architecture

Many popular systems leverage a microservice architecture where individual services exist to handle individual features. Each component should be able to be deployed separately and interopable such that any one service in any one language could be deployed along side any other service written in any other language. These services should include:
* One service per API type
* One worker service to handle a long running asynchronous operation

#### Multi-threaded

In addition to microservices, at least one API service should have a secondary "worker" thread to demonstrate communicating across threads to do work.

#### APIs

One common data schema should be defined that can be serviced by multiple API types. As much as possible, each API should support the same functionality. Each API should:
* Support CRUD operations for the data model
* Provide at least two "long running" operations which have an asynchronous response, one to be run in a secondary worker thread of the API service, and another to be handled by the separate worker service
* Provide at least one operation which has a synchronous response

The following API types should be supported:
* REST
* GraphQL
* Websocket

#### Event Driven

The communication between the APIs and the Worker Service should be event driven.

#### Unit Tests

Unit tests must be written with as near 100% coverage as possible.

### Language Support

| Language | REST    | GraphQL | Websocket | WorkerService | Tests   |
| -------- | ------- | ------- | --------- | ------------- | ------- |
| Go       | &cross; | &cross; | &cross;   | &cross;       | &cross; |
| Java     | &cross; | &cross; | &cross;   | &cross;       | &cross; |
| Python   | &cross; | &cross; | &cross;   | &cross;       | &cross; |
| Rust     | &cross; | &cross; | &cross;   | &cross;       | &cross; |
| Scala    | &cross; | &cross; | &cross;   | &cross;       | &cross; |
