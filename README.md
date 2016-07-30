# Vert.x GraphQL Test data

[![Apache licensed](https://img.shields.io/hexpm/l/plug.svg?maxAge=2592000)](https://github.com/engagingspaces/vertx-graphql-testdata/blob/master/LICENSE)&nbsp;&nbsp;
[ ![Download](https://api.bintray.com/packages/engagingspaces/maven/vertx-test-graphql-starwars-client/images/download.svg) ](https://bintray.com/engagingspaces/maven/vertx-test-graphql-starwars-client/_latestVersion)

This project contains test data and example code that is used in various Vert.x GraphQL projects:

- [vertx-graphql-service-discovery](https://github.com/engagingspaces/vertx-graphql-service-discovery)
  - [vertx-graphql-servicediscovery-core](https://github.com/engagingspaces/vertx-graphql-service-discovery/grapql-servicediscovery-core) (sub-project)
  - [vertx-graphql-schema-publisher](https://github.com/engagingspaces/vertx-graphql-service-discovery/vertx-graphql-schema-publisher) (sub-project)
  - [vertx-graphql-schema-consumer](https://github.com/engagingspaces/vertx-graphql-service-discovery/vertx-graphql-schema-consumer) (sub-project)

- [vertx-graphql-schema-proxy](https://github.com/engagingspaces/vertx-schema-proxy)
  - [vertx-graphql-json-marshaller](https://github.com/engagingspaces/vertx-schema-proxy/vertx-graphql-json-marshaller) (sub-project)
  - [vertx-graphql-service-proxy](https://github.com/engagingspaces/vertx-schema-proxy/vertx-graphql-service-proxy) (sub-project)

## Using

You can just check out the code and then:

```
gradle clean build
```

Or get dependenciies from Bintray using Maven:

```
<?xml version="1.0" encoding="UTF-8" ?>
<settings xsi:schemaLocation='http://maven.apache.org/SETTINGS/1.0.0
              http://maven.apache.org/xsd/settings-1.0.0.xsd'
          xmlns='http://maven.apache.org/SETTINGS/1.0.0'
              xmlns:xsi='http://www.w3.org/2001/XMLSchema-instance'>

    <dependencies>
        <dependency>
            <groupId>io.engagingspaces</groupId>
            <artifactId>vertx-test-graphql-droids-microservice</artifactId>
            <version>0.9.2</version>
        </dependency>
        <dependency>
            <groupId>io.engagingspaces</groupId>
            <artifactId>vertx-test-graphql-starwars-microservice</artifactId>
            <version>0.9.2</version>
        </dependency>
        <dependency>
            <groupId>io.engagingspaces</groupId>
            <artifactId>vertx-test-graphql-starwars-client</artifactId>
            <version>0.9.2</version>
        </dependency>
    </dependencies>

    <profiles>
        <profile>
            <repositories>
                <repository>
                    <snapshots>
                        <enabled>false</enabled>
                    </snapshots>
                    <id>bintray-engagingspaces-maven</id>
                    <name>bintray</name>
                    <url>http://dl.bintray.com/engagingspaces/maven</url>
                </repository>
            </repositories>
            <pluginRepositories>
                <pluginRepository>
                    <snapshots>
                        <enabled>false</enabled>
                    </snapshots>
                    <id>bintray-engagingspaces-maven</id>
                    <name>bintray-plugins</name>
                    <url>http://dl.bintray.com/engagingspaces/maven</url>
                </pluginRepository>
            </pluginRepositories>
            <id>bintray</id>
        </profile>
    </profiles>
    <activeProfiles>
        <activeProfile>bintray</activeProfile>
    </activeProfiles>
</settings>
```


Or when using Gradle:

```
repositories {
  maven {
    url "http://dl.bintray.com/engagingspaces/maven"
  }
}

dependencies {
  compile 'io.engagingspaces:vertx-test-graphql-droids-microservice:0.9.2'
  compile 'io.engagingspaces:vertx-test-graphql-starwars-microservice:0.9.2'
  compile 'io.engagingspaces:vertx-test-graphql-starwars-client:0.9.2'
}
```

## Acknowledgments

The test data in this library was converted from Groovy data in the
[graphql-java](https://github.com/graphql-java/graphql-java) project created by Andreas Marek.

## License

This project [vertx-graphql-testdata](https://github.com/engagingspaces/vertx-graphql-testdata) is licensed
under the [Apache Commons v2.0](https://github.com/engagingspaces/vertx-graphql-service-discovery/LICENSE) license.

Copyright &copy; 2016 Arnold Schrijver and other
[contributors](https://github.com/engagingspaces/vertx-graphql-testdata/graphs/contributors)
