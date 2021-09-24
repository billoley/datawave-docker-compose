# DATAWAVE Docker Compose

## Components

### Discovery (Consul)

Consul v1.9.8 is a prepacked docker image used for discovery between the various services.

### Messaging (RabbitMQ)

RabbitMQ v3.7.7 is a prepacked docker image used for messaging between the various services.

### Configuration

[Datawave Config Service v1.4](https://github.com/NationalSecurityAgency/datawave-config-service/releases/tag/1.4) is Datawave's customized Spring Cloud config service.

Sample configuration files can be found in the config folder.

You will need to build the docker image for this service on your local machine following the instructions in the config service README.

### Cache

[Datawave Hazelcast Service v1.4](https://github.com/NationalSecurityAgency/datawave-hazelcast-service/releases/tag/service-1.6) is Datawave's customized Hazelcast In-Memory Data Grid.

You will need to build the docker image for this service on your local machine following the instructions in the config service README.

### Authorization

[Datawave Authorization Service v1.9](https://github.com/NationalSecurityAgency/datawave-authorization-service/releases/tag/service-1.9) provides basic authorization for the Datawave microservices.

You will need to build the docker image for this service on your local machine following the instructions in the config service README.

### Audit

[Datawave Audit Service v1.9](https://github.com/NationalSecurityAgency/datawave-audit-service/releases/tag/service-1.9) provides query audit capabilities for Datawave.

You will need to build the docker image for this service on your local machine following the instructions in the config service README.

## Usage

You will need to have Zookeeper, Hadoop HDFS, and Accumulo running 

### Start services

```docker-compose up -d```

### View logs

For everything:

```docker-compose logs -f```

For a specific service:

```docker-compose logs -f audit```

### Stop services

```docker-compose down```

UIs

Consul - http://localhost:8500
Fabio - http://localhost:8000
RabbitMQ - http://localhost:15672 (u:guest p:guest)




