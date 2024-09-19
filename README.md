# quarkus-archi-grpc

This project uses Quarkus, the Supersonic Subatomic Java Framework.

If you want to learn more about Quarkus, please visit its website: <https://quarkus.io/>.

## Running the application in dev mode

You can run your application in dev mode that enables live coding using:

```shell script
./mvnw compile quarkus:dev
```

> **_NOTE:_**  Quarkus now ships with a Dev UI, which is available in dev mode only at <http://localhost:8080/q/dev/>.

## Packaging and running the application

The application can be packaged using:

```shell script
./mvnw package
```

It produces the `quarkus-run.jar` file in the `target/quarkus-app/` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/quarkus-app/lib/` directory.

The application is now runnable using `java -jar target/quarkus-app/quarkus-run.jar`.

If you want to build an _über-jar_, execute the following command:

```shell script
./mvnw package -Dquarkus.package.jar.type=uber-jar
```

The application, packaged as an _über-jar_, is now runnable using `java -jar target/*-runner.jar`.

## Creating a native executable

You can create a native executable using:

```shell script
./mvnw package -Dnative
```

Or, if you don't have GraalVM installed, you can run the native executable build in a container using:

```shell script
./mvnw package -Dnative -Dquarkus.native.container-build=true
```

You can then execute your native executable with: `./target/quarkus-archi-grpc-1.0.0-SNAPSHOT-runner`

If you want to learn more about building native executables, please consult <https://quarkus.io/guides/maven-tooling>.

## Related Guides

- Camel gRPC ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/grpc.html)): Expose gRPC endpoints and access external gRPC endpoints
- Citrus ([guide](https://github.com/christophd/citrus-demo-quarkus)): Add Citrus support to your Quarkus tests. Citrus is an Open Source Java integration testing framework supporting a wide range of message protocols and data formats (Kafka, Http REST, JMS, TCP/IP, SOAP, FTP/SFTP, XML, Json, and more)
- Camel Jasypt ([guide](https://camel.apache.org/camel-quarkus/latest/reference/extensions/jasypt.html)): Security using Jasypt
- Flyway ([guide](https://quarkus.io/guides/flyway)): Handle your database schema migrations
- Dashbuilder ([guide](https://quarkiverse.github.io/quarkiverse-docs/quarkus-dashbuilder/dev/index.html)): Dashbuilder extension for embedding dashboards in a Quarkus application
- Elasticsearch Java Client ([guide](https://quarkus.io/guides/elasticsearch)): Connect to an Elasticsearch cluster using the Java client
- Dapr ([guide](https://quarkiverse.github.io/quarkiverse-docs/quarkus-dapr/dev/index.html)): Dapr SDK
- Microcks ([guide](https://github.com/microcks/microcks-quarkus)): Microcks is an open-source cloud-native platform for mocking and contract-testing all kinds of APIs - directly from your specs. It supports REST OpenAPI, gRPC, GraphQL, Async APIs and SOAP WebServices.

## Provided Code

### gRPC

Create your first gRPC service

[Related guide section...](https://quarkus.io/guides/grpc-getting-started)
