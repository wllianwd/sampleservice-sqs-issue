# Overview

## Prerequisite

* Maven
* Java 17

## How to test

```
# bring localstack up
docker-compose up

# run service
mvn spring-boot:run
```

## Error

```
org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'sqsSampleProducer' defined in file [../target/classes/com/test/sampleservice/SqsSampleProducer.class]: Unsatisfied dependency expressed through constructor parameter 0: Error creating bean with name 'sqsAsyncClient' defined in class path resource [io/awspring/cloud/autoconfigure/sqs/SqsAutoConfiguration.class]: Failed to instantiate [software.amazon.awssdk.services.sqs.SqsAsyncClient]: Factory method 'sqsAsyncClient' threw exception with message: Expected a profile or property definition on line 1
        at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:798) ~[spring-beans-6.0.3.jar:6.0.3]
        at org.springframework.beans.factory.support.ConstructorResolver.autowireConstructor(ConstructorResolver.java:245) ~[spring-beans-6.0.3.jar:6.0.3]
        ...
```