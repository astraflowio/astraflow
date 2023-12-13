![Conductor](docs/docs/img/logo.png)

## Announcement

> Effective **December 13, 2023**, Netflix will discontinue maintenance of Conductor OSS on GitHub. This strategic decision, while difficult, is essential for realigning our resources to better serve our business objectives > with our internal Conductor fork.
> We are *deeply grateful* for your support and contributions over the years. While Netflix will no longer be maintaining this repo, members of the Conductor community have been active in promoting alternative forks of this > project, we’ll leave the code as is and trust that the health of the community will remain strong and continue to develop moving forward.


# Conductor
[![Github release](https://img.shields.io/github/v/release/Netflix/conductor.svg)](https://GitHub.com/Netflix/conductor/releases)
[![License](https://img.shields.io/github/license/Netflix/conductor.svg)](http://www.apache.org/licenses/LICENSE-2.0)

[![GitHub stars](https://img.shields.io/github/stars/Netflix/conductor.svg?style=social&label=Star&maxAge=2592000)](https://GitHub.com/Netflix/conductor/stargazers/)
[![GitHub forks](https://img.shields.io/github/forks/Netflix/conductor.svg?style=social&label=Fork&maxAge=2592000)](https://GitHub.com/Netflix/conductor/network/)

Conductor is a platform created by Netflix to orchestrate workflows that span across microservices.
Conductor is maintained by Media Workflow Infrastructure team at Netflix.

## Releases
The final release is [![Github release](https://img.shields.io/github/v/release/Netflix/conductor.svg)](https://GitHub.com/Netflix/conductor/releases)

[2.31.8](https://github.com/Netflix/conductor/releases/tag/v2.31.8) is the **final** release of `2.31` branch. As of Feb 2022, `1.x` & `2.x` versions are no longer supported.

## Workflow Creation in Code
Conductor supports creating workflows using JSON and Code.  
SDK support for creating workflows using code is available in multiple languages and can be found at https://github.com/conductor-sdk

## Community Contributions
The modules contributed by the community are housed at [conductor-community](https://github.com/Netflix/conductor-community). Compatible versions of the community modules are released simultaneously with releases of the main modules.

[Discussion Forum](https://github.com/Netflix/conductor/discussions): Please use the forum for questions and discussing ideas and join the community.

[List of Conductor community projects](/docs/docs/resources/related.md): Backup tool, Cron like workflow starter, Docker containers and more.

## Getting Started - Building & Running Conductor
###  Using Docker:
The easiest way to get started is with Docker containers. Please follow the instructions [here](https://conductor.netflix.com/devguide/running/docker.html). 

###  From Source:
Conductor Server is a [Spring Boot](https://spring.io/projects/spring-boot) project and follows all applicable conventions. See instructions [here](https://conductor.netflix.com/devguide/running/source.html).

## Published Artifacts
Binaries are available from the [Maven Central Repository](https://search.maven.org/search?q=g:com.netflix.conductor).

| Artifact                        | Description                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------|
| conductor-common                | Common models used by various conductor modules                                                 |
| conductor-core                  | Core Conductor module                                                                           |
| conductor-redis-persistence     | Persistence and queue using Redis/Dynomite                                                      |
| conductor-cassandra-persistence | Persistence using Cassandra                                                                     |
| conductor-es6-persistence       | Indexing using Elasticsearch 6.X                                                                |
| conductor-rest                  | Spring MVC resources for the core services                                                      |
| conductor-ui                    | node.js based UI for Conductor                                                                  |
| conductor-client                | Java client for Conductor that includes helpers for running worker tasks                        |
| conductor-client-spring         | Client starter kit for Spring                                                                   |
| conductor-java-sdk              | SDK for writing workflows in code                                                               |
| conductor-server                | Spring Boot Web Application                                                                     |
| conductor-redis-lock            | Workflow execution lock implementation using Redis                                              |
| conductor-awss3-storage         | External payload storage implementation using AWS S3                                            |
| conductor-awssqs-event-queue    | Event queue implementation using AWS SQS                                                        |
| conductor-http-task             | Workflow system task implementation to send make requests                                       |
| conductor-json-jq-task          | Workflow system task implementation to evaluate JSON using [jq](https://stedolan.github.io/jq/) |
| conductor-grpc                  | Protobuf models used by the server and client                                                   |
| conductor-grpc-client           | gRPC client to interact with the gRPC server                                                    |
| conductor-grpc-server           | gRPC server Application                                                                         |
| conductor-test-harness          | Integration and regression tests                                                                |

## Database Requirements

* The default persistence used is Redis
* The indexing backend is [Elasticsearch](https://www.elastic.co/) (6.x)

## Other Requirements
* JDK 17+
* UI requires Node 14 to build. Earlier Node versions may work but is untested.

## Get Support
There are several ways to get in touch with us:
* [Slack Community](https://join.slack.com/t/orkes-conductor/shared_invite/zt-xyxqyseb-YZ3hwwAgHJH97bsrYRnSZg)
* [GitHub Discussion Forum](https://github.com/Netflix/conductor/discussions)

## Contributions
Whether it is a small documentation correction, bug fix or a new feature, contributions are highly appreciated. We just ask you to follow standard OSS guidelines. The [Discussion Forum](https://github.com/Netflix/conductor/discussions) is a good place to ask questions, discuss new features and explore ideas. Please check with us before spending too much time, only to find out later that someone else is already working on a similar feature.

`main` branch is the current working branch. Please send your PR's to `main` branch, making sure that it builds on your local system successfully. Also, please make sure all the conflicts are resolved.

## License
Copyright 2022 Netflix, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
