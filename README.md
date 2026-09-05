<div align="center">
<h1>Awesome Camunda Platform 8</h1>

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![Contribute](https://img.shields.io/badge/contribute-project-blue.svg)](https://github.com/camunda-community-hub/awesome-camunda-platform-8/pulls) ⭐ 142 | 🐛 3 | 📅 2024-05-02 [![](https://img.shields.io/badge/Community%20Extension-An%20open%20source%20community%20maintained%20project-FF4700)](https://github.com/camunda-community-hub/community) ⭐ 23 | 🐛 1 | 📅 2025-12-09 ![](https://img.shields.io/badge/Compatible%20with-Camunda%20Platform%208-0072Ce)

<hr />
<a href="https://camunda.com/platform/">Camunda Platform 8</a>&nbsp;&nbsp;&nbsp;
<a href="CODE_OF_CONDUCT.md">Code of Conduct</a>&nbsp;&nbsp;&nbsp;
<a href="CONTRIBUTING.md">Contributing</a>
<hr />
</div>

A curated list of awesome [Camunda Platform 8](https://camunda.com/platform/) projects, mostly driven by the community. Inspired by [awesome-go](https://github.com/avelino/awesome-go) ⭐ 183,257 | 🐛 223 | 🌐 Go | 📅 2026-09-05.

Previously, this list contained only Zeebe awesome-ness. Help us collect all things awesome about Camunda Platform 8 and Zeebe, the workflow engine powering Camunda Platform 8.

## Contents

* [Contents](#contents)
* [Clients and Programming Framework Integrations](#clients-and-programming-framework-integrations)
* [Connectors and Bridges](#connectors-and-bridges)
* [Job Workers](#job-workers)
* [Exporters](#exporters)
* [Applications](#applications)
* [Testing](#testing)
* [Others](#others)
* [Contributing](#contributing)
* [License](#license)

# Awesome Projects with stars

## Clients and Programming Framework Integrations

Client libraries to interact with Camunda Platform 8 and Zeebe

* [Java](https://github.com/camunda/zeebe/tree/main/clients/java) ⭐ 4,270 | 🐛 2,943 | 🌐 Java | 📅 2026-09-05
  * [Spring](https://github.com/camunda-community-hub/spring-zeebe) ⭐ 215 | 🐛 13 | 🌐 Java | 📅 2026-09-04
  * [Micronaut](https://github.com/camunda-community-hub/micronaut-zeebe-client) ⭐ 28 | 🐛 7 | 🌐 Java | 📅 2026-03-20
* [Go](https://github.com/camunda-cloud/zeebe/tree/master/clients/go) ⭐ 4,270 | 🐛 2,943 | 🌐 Java | 📅 2026-09-05
* [Node.js](https://github.com/camunda-community-hub/zeebe-client-node-js) ⚠️ Archived
  * [NestJS](https://github.com/camunda-community-hub/nestjs-zeebe#readme) ⭐ 28 | 🐛 0 | 🌐 TypeScript | 📅 2024-02-01
* [C#](https://github.com/camunda-community-hub/zeebe-client-csharp) ⭐ 114 | 🐛 38 | 🌐 C# | 📅 2026-09-05
* [WorkIt](https://github.com/VilledeMontreal/workit) ⭐ 62 | 🐛 2 | 🌐 TypeScript | 📅 2026-09-03 - Node.js (TypeScript) client for both Zeebe and Camunda BPM platforms (Not updated for Zeebe 1.0.0)
* [Rust](https://github.com/camunda-community-hub/zeebest) ⭐ 21 | 🐛 13 | 🌐 Rust | 📅 2025-08-20
* [Delphi](https://github.com/camunda-community-hub/DelphiZeeBeClient) ⭐ 9 | 🐛 1 | 🌐 Pascal | 📅 2023-12-15
* [Ruby](https://github.com/zeebe-io/zeebe-client-ruby) ⚠️ Archived
  * [Beez](https://github.com/gottfrois/beez) ⭐ 9 | 🐛 11 | 🌐 Ruby | 📅 2023-01-19 - Simple, efficient ruby workers for Zeebe (Not updated for Zeebe 1.0.0)
* Python:
  * [Pyzeebe](https://github.com/camunda-community-hub/pyzeebe) ⭐ 101 | 🐛 23 | 🌐 Python | 📅 2026-09-05
  * [Zeebe Python gRPC](https://pypi.org/project/zeebe-grpc/)

**Want a client for another language?**

Thanks to gRPC you can generate client stubs easily as described in [Generating a Zeebe-Python Client Stub in Less Than An Hour: A gRPC + Zeebe Tutorial](https://camunda.com/blog/2018/11/grpc-generating-a-zeebe-python-client/).

## Connectors and Bridges

Connector: A reusable building block that performs the integration with an external system and works out of the box.

* [Awesome Camunda Platform 8 Connectors](https://github.com/camunda-community-hub/camunda-8-connectors) ⭐ 40 | 🐛 0 | 📅 2025-03-31 -- all connectors, whether created by Camunda, the community, or partners, are listed here.

Bridge: A piece of software that connects Camunda Platform 8 or Zeebe with some other system or infrastructure. Might be uni or bidirectional and possibly includes a job worker.

* [Kafka Connector](https://github.com/camunda-community-hub/kafka-connect-zeebe) ⭐ 99 | 🐛 36 | 🌐 Java | 📅 2025-06-05
* [Node-RED Zeebe nodes](https://github.com/camunda-community-hub/node-red-contrib-zeebe) ⭐ 26 | 🐛 31 | 🌐 JavaScript | 📅 2023-12-15
* [Lambda](https://github.com/camunda-community-hub/zeebe-lambda-worker) ⭐ 8 | 🐛 4 | 🌐 Java | 📅 2023-12-15 - A Zeebe worker to invoke AWS Lambdas (Serverless functions), allowing to orchestrate functions
* [Zeebe GitHub Action](https://github.com/marketplace/actions/camunda-8-action) - Integrate Zeebe into GitHub Workflows with Camunda Platform 8

## Job Workers

Job Worker: A special type of client that polls for and executes available jobs. In contrast to connectors and bridges, such workers do not connect to other active pieces of software primarily (for example, a 'DMN Connector' might connect Zeebe to a managed DMN Engine, a 'DMN worker' will use a DMN library to execute decisions).

* [DMN Scala](https://github.com/camunda/dmn-scala/) ⭐ 42 | 🐛 26 | 🌐 Scala | 📅 2026-09-04 - Zeebe job worker using the Scala DMN engine
* [Script](https://github.com/camunda-community-hub/zeebe-script-worker) ⭐ 33 | 🐛 1 | 🌐 Java | 📅 2026-09-05 - Zeebe job worker for evaluating JS, Groovy, Kotlin and FEEL scripts
* [Camunda DMN](https://github.com/camunda-community-hub/zeebe-dmn-worker) ⭐ 19 | 🐛 0 | 🌐 Java | 📅 2026-02-03 - Zeebe job worker using the Camunda DMN engine
* [Zeebe Slack Worker](https://github.com/camunda-community-hub/zeebe-slack-worker) ⭐ 4 | 🐛 11 | 🌐 TypeScript | 📅 2023-12-15 - A Node.js library for building job workers that send messages to Slack based on service tasks.

## Exporters

Exporters to load data into external systems, only available with Camunda Platform 8 Self-Managed.

* [Elasticsearch](https://github.com/camunda/zeebe/tree/main/exporters/elasticsearch-exporter) ⭐ 4,270 | 🐛 2,943 | 🌐 Java | 📅 2026-09-05
* [Hazelcast](https://github.com/camunda-community-hub/zeebe-hazelcast-exporter) ⭐ 49 | 🐛 10 | 🌐 Java | 📅 2026-04-13
* [Kafka](https://github.com/camunda-community-hub/zeebe-kafka-exporter) ⭐ 37 | 🐛 39 | 🌐 Java | 📅 2025-06-23
* [Incident Alerter (Webhook)](https://github.com/jwulf/zeebe-incident-alerter) ⭐ 7 | 🐛 1 | 🌐 Kotlin | 📅 2024-12-19
* [MongoDB](https://github.com/crossid/zeebe-mongo-exporter) ⭐ 7 | 🐛 0 | 🌐 Java | 📅 2024-10-31
* [Event Store](https://github.com/jwulf/zeebe-eventstore-exporter) ⭐ 6 | 🐛 4 | 🌐 Java | 📅 2024-06-24
* [CSV](https://github.com/zeebe-io/zeebe-csv-exporter) ⚠️ Archived
* [NATS Streaming Server](https://github.com/MrSaints/zeebe-nats-streaming-exporter) ⚠️ Archived

**Want an exporter for another system?**

You can build one in as little as 15 minutes. Take a look at the [Zeebe Exporter Demo](https://github.com/jwulf/zeebe-exporter-demo) ⭐ 7 | 🐛 3 | 🌐 Java | 📅 2021-02-05, and the tutorial blog posts [Part One](https://camunda.com/blog/2019/05/exporter-part-1/) and [Part Two](https://camunda.com/blog/2019/06/exporter-part-2/).

## Applications

Applications to interact with Camunda Platform 8 and Zeebe

* [Simple Monitor](https://github.com/camunda-community-hub/zeebe-simple-monitor) ⭐ 180 | 🐛 38 | 🌐 Java | 📅 2026-04-11 - A lightweight application for monitoring and interacting with Zeebe during development
* [Zeebe Simple Tasklist](https://github.com/camunda-community-hub/zeebe-simple-tasklist) ⭐ 75 | 🐛 3 | 🌐 Java | 📅 2025-06-05 - Zeebe job worker for manual/user tasks
* [ZeeQS](https://github.com/camunda-community-hub/zeeqs) ⭐ 61 | 🐛 14 | 🌐 Kotlin | 📅 2025-06-05 - GraphQL query API for aggregated Zeebe data
* [Quintessential Task List](https://github.com/StephenOTT/Quintessential-Tasklist-Zeebe) ⭐ 36 | 🐛 21 | 🌐 Java | 📅 2020-02-11 - The quintessential Zeebe tasklist for BPMN Human tasks with Drag and Drop Form builder, client and server side validations, and drop in Form Rendering
* [Workflow Linter](https://github.com/StephenOTT/Workflow-Linter) ⭐ 15 | 🐛 2 | 🌐 Kotlin | 📅 2020-02-11 - Workflow Linter for BPMN workflows
* [Python-Zeebe Sandbox](https://github.com/nimanamjouyan/python-zeebe) ⭐ 12 | 🐛 0 | 🌐 Python | 📅 2021-06-01 - A FastAPI python sandbox for Zeebe to deploy workflows, run instances and publish messages. This dockerised app runs Zeebe Simple Monitor, a single node Zeebe broker and a FastAPI python container to allow exploration/investigation of Zeebe features and workflows.
* [Zeebe Cloud Canary](https://github.com/jwulf/zeebe-cloud-canary) ⭐ 4 | 🐛 6 | 🌐 TypeScript | 📅 2021-08-11 - Monitor the aliveness of a Zeebe broker
* [zbctl](https://docs.camunda.io/docs/apis-clients/cli-client/) - CLI to interact with Zeebe
* [zbctl via npm](https://www.npmjs.com/package/zbctl) - zbctl is just an `npm install` away
* [zbctl via Homebrew](https://formulae.brew.sh/formula/zbctl) - zbctl from the famous Mac OS package manager
* [zbctl via Snap](https://snapcraft.io/zbctl) - Install zbctl through your Linux package manager, e.g. `snap install zbctl`
* [dockerised zbctl](https://hub.docker.com/r/sitapati/zbctl) - See [these notes on using it in CI](https://forum.zeebe.io/t/use-docker-compose-cant-find-bpmn-file/1004/3?u=jwulf)

## Testing

Test utilities to help you develop Camunda Platform 8 or Zeebe-dependent applications

* [BPMN Spec](https://github.com/camunda-community-hub/bpmn-spec) ⭐ 29 | 🐛 12 | 🌐 Kotlin | 📅 2024-10-25 - a tool to write tests for BPMN workflows on run them on Zeebe
* [Zeebe Test Container](https://github.com/camunda-community-hub/zeebe-test-container) ⭐ 24 | 🐛 17 | 🌐 Java | 📅 2026-09-04 - [TestContainers](https://testcontainers.org) module to help you write integration tests against configurable Zeebe instances.
* [Benchmark Helm Profile](https://github.com/camunda-community-hub/camunda-8-helm-profiles/tree/main/google/benchmark) ⭐ 24 | 🐛 37 | 🌐 Makefile | 📅 2026-07-29 - a Helm chart configuration for benchmarking.
* [Zeebe Chaos](https://github.com/zeebe-io/zeebe-chaos) ⭐ 23 | 🐛 46 | 🌐 Go | 📅 2026-09-02 - contains everything related to chaos engineering and Zeebe, like chaos experiments, an hypotheses backlog etc.
* [Camunda 8 Benchmark (c8b)](https://github.com/camunda-community-hub/camunda-8-benchmark) ⭐ 21 | 🐛 38 | 🌐 Java | 📅 2026-09-04 - a load generator for Zeebe.
* [Zeebe Worker Java Testutils](https://github.com/camunda-community-hub/zeebe-worker-java-testutils) ⭐ 9 | 🐛 9 | 🌐 Java | 📅 2025-06-05 - Utilities to test Zeebe workers implemented in Java
* [Zeebe BPMN RSpec](https://github.com/ezcater/zeebe_bpmn_rspec) ⭐ 5 | 🐛 4 | 🌐 Ruby | 📅 2026-04-16 - Ruby gem to test workflow logic in Zeebe using RSpec.
* [Zeebe Tuner](https://github.com/camunda-consulting/zeebe-tuner/) ⭐ 4 | 🐛 11 | 🌐 Java | 📅 2026-08-06 - an iterative benchmark runner parameterized using a spreadsheet.
* [Zeebe Performance Benchmarking / Tuning Tool](https://zeebe.io/blog/2020/11/zeebe-performance-tool/) - a performance benchmarking and tuning spreadsheet from Camunda solution architect Falko Menge.

## Others

Other Camunda Platform 8 & Zeebe related applications

* [FEEL REPL](https://camunda.github.io/feel-scala/docs/reference/#feel-repl) - easily try FEEL expressions using the REPL (Read-Eval-Print-Loop) of the [FEEL Scala engine](https://github.com/camunda/feel-scala) ⭐ 136 | 🐛 45 | 🌐 Scala | 📅 2026-09-04.
* [zdb](https://github.com/Zelldon/zdb) ⭐ 34 | 🐛 33 | 🌐 Java | 📅 2026-09-05 - Zeebe debug and inspection tool, allows to inspect the log and internal state of Zeebe.
* [zeebe-worker-java-template](https://github.com/camunda-community-hub/zeebe-worker-java-template) ⭐ 4 | 🐛 0 | 🌐 Java | 📅 2023-12-15 - Minimal template for a [Zeebe](https://github.com/camunda-cloud/zeebe) ⭐ 4,270 | 🐛 2,943 | 🌐 Java | 📅 2026-09-05
  Java [worker](https://docs.camunda.io/docs/components/concepts/job-workers/). This template adds only the bare minimum of dependencies.
* [Helm Charts](https://helm.camunda.io/) - [Helm](https://helm.sh/) charts to deploy Zeebe to Kubernetes.
* [Portainer Templates](https://camunda-community-hub.github.io/zeebe-portainer-templates/) - [Portainer](https://www.portainer.io/) templates to deploy Zeebe to Docker.

## Contributing

Please help us keep this list up to date! PRs welcome, follow our [contribution guidelines](CONTRIBUTING.md).

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0)

To the extent possible under law, Zeebe has waived all copyright and related or neighboring rights to this work.

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-09-05._
