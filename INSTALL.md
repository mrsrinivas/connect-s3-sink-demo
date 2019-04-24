# Setup instructions on Linux/OS X

Before proceed with instructions make sure Java 1.8+ is installed and configured in `PATH`

**Download the Confluent distribution of Kafka** 

```bash
  $ wget http://packages.confluent.io/archive/5.2/confluent-5.2.0-2.12.tar.gz
```

**Setup Kafka**

```bash
  $ tar -xzf confluent-5.2.0-2.12.tar.gz 
  $ cd confluent-5.2.0-2.12
```

**Verify installation**

```bash
  $ ./bin/confluent list
  Available services:
    zookeeper
    kafka
    schema-registry
    kafka-rest
    connect
    ksql-server
    control-center  
```

**Install connect datagen**

[_datagen_](https://github.com/confluentinc/kafka-connect-datagen/tree/master) is one of the easiest way to generate the data into Kafka (producer/connect source).
Let's install it to pump some data into into Kafka.

```bash
  $ confluent-hub install confluentinc/kafka-connect-datagen:latest
```

**Start services**
```bash
  $ confluent start connect
  This CLI is intended for development only, not for production
  https://docs.confluent.io/current/cli/index.html
  
  Using CONFLUENT_CURRENT: /some/path/in/local/machine
  Starting zookeeper
  zookeeper is [UP]
  Starting kafka
  kafka is [UP]
  Starting schema-registry
  schema-registry is [UP]
  Starting connect
  connect is [UP]
```
make sure services are **UP**

