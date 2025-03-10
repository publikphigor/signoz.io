---
title: Current state of OpenTelemetry and how it fits in the DevOps ecosystem | Q&A
slug: current-state-of-opentelemetry
date: 2022-09-21
tags: [Talks]
authors: [ankit_anand]
description: OpenTelemetry is quietly becoming the world standard for instrumenting cloud-native applications.To understand complex distributed systems, DevOps engineers need to implement a robust observability & monitoring framework. OpenTelemetry provides vendor-neutral open source observability framework...
image: /img/blog/2022/09/current_state_of_opentelemetry_cover.webp
keywords:
  - kubernetes
  - kubernetes metrics server
  - Kubernetes metrics
  - kubernetes audit policy
---

<head>
  <link rel="canonical" href="https://signoz.io/blog/current-state-of-opentelemetry/"/>
</head>

OpenTelemetry is an open-source project under the Cloud Native Computing Foundation(<a href="https://www.cncf.io/" rel="nofollow">CNCF</a>) that aims to standardize the generation and collection of telemetry data. The telemetry data helps developer, DevOps and IT teams to keep a check on their application health.

The telemetry data collected by OpenTelemetry consist of logs, metrics, and traces. Together, they are used for performance monitoring and observability in distributed systems. 

<!--truncate-->

![Cover Image](/img/blog/2022/09/current_state_of_opentelemetry_cover.webp)

At SigNoz, we are building an OpenTelemetry native APM. We believe in the mission of ubiquitous observability with OpenTelemetry. Managing distributed systems at scale is a pain, and OpenTelemetry aims to solve a lot of pain points for developers and devops folks.

I sat down with <a href="https://www.linkedin.com/in/pranay01/" rel="nofollow">Pranay</a>, the CEO and co-founder at SigNoz to discuss the current state of OpenTelemetry and how it fits in the DevOps ecosystem. 


### Do you think OpenTelemetry is (or will be) important to IT Ops/DevOps, and why?

**Pranay:** OpenTelemetry is quietly becoming the world standard for instrumenting cloud-native applications. Cloud computing and containerization have benefits like on-demand scaling, but they have also increased the complexity of IT Ops and DevOps manifolds.

To understand complex distributed systems, DevOps engineers need to implement a robust observability & monitoring framework. OpenTelemetry provides vendor-neutral open source observability framework for generating and collecting important telemetry signals.

Two important reasons that make OpenTelemetry important to IT Ops are:

- **OpenTelemetry makes your instrumentation future-proof**<br></br>
OpenTelemetry is an open standard and open source implementation with contributors from companies like AWS, Microsoft, Splunk, etc. It provides instrumentation libraries in almost all major programming languages and covers most of the popular open source frameworks. If tomorrow your team decides to use a new open source library in the tech stack, you can have the peace of mind that Opentelemetry will provide instrumentation for it.

- **It is vendor-neutral and supports different telemetry signals like metrics, traces, logs, events**<br></br>
Opentelemetry is the instrumentation standard. You can use any backend & storage layer to store telemetry data and frontend to visualize that data.
So as long as these components support the OTLP format ( OpenTelemetry’s format), they can process and visualize OTel data

### What do you see as the main business benefits OpenTelemetry will ultimately deliver?

**Pranay:** The main business benefit that we see from using OpenTelemetry is that it is future-proof. Open source has changed the way software is getting developed, and you can expect OpenTelemetry to constantly evolve and get updated as it is driven by a community.

Another business benefit that we see is no vendor lock-in. Users don’t get vendor locked-in as they can change the vendor they use for storing and visualizing data very easily as long as it supports OTel format. It also makes a level playing field for new products to emerge. 

No vendor lock-in also means more control over observability costs. The freedom to choose an observability vendor of your choice while having access to world-class instrumentation is a huge advantage to the business.

Another advantage that we see is the cost associated with ramping up your engineering team. Using an open source standard helps engineering teams to create a knowledge base that is consistent and improves with time. 

### When do you foresee OpenTelemetry becoming a significant solution in IT Ops/DevOps?

**Pranay:** OpenTelemetry is already being widely adopted by the community. Most observability vendors provide support for OpenTelemetry data formats. But as it’s a huge initiative, we expect it to reach maturity in most signals in the next one to two years.

### What are the barriers or shortfalls to OpenTelemetry?

**Pranay:** OpenTelemetry provides instrumentation to generate logs, metrics, and traces. Tracing is stable in almost all languages. Metrics is stable and generally available in Java/Python/Dotnet and RC/Beta in other important languages. Logs is experimental in Java/Python/Dotnet. Though you can use the OpenTelemetry collector to collect logs from your existing pipelines.

OpenTelemetry is developing at a fast rate, and the instrumentation is rapidly changing. This can lead to frustrating bugs at times. The community is also taking steps to address concerns around <a href="https://github.com/open-telemetry/opentelemetry-specification/issues/2753" rel="nofollow">instrumentation stability</a>. 

### What advice do you give to an IT organization that wants to start working with OpenTelemetry now?

**Pranay:** We would suggest they start instrumenting a service or two and play with the data using a visualization tool. If you’re just starting your observability journey, you can use the auto-instrumentation libraries provided by OpenTelemetry. For example, OpenTelemetry provides a handy [Java Jar agent](https://signoz.io/opentelemetry/java-agent/) which enables Java applications to generate and capture telemetry data automatically.

For companies using Kubernetes, we would suggest using [OpenTelemetry operators](https://signoz.io/docs/tutorial/opentelemetry-operator-usage/) which makes it very easy to set up Collector and instrument workloads deployed on Kubernetes.

OpenTelemetry also provides a stand-alone service called the  [OpenTelemetry Collector](https://signoz.io/blog/opentelemetry-collector-complete-guide/). You can use it as a telemetry processing system. It can also collect host metrics such as RAM, CPU, and storage capacity automatically.

### How does APM fit in with OpenTelemetry?

**Pranay:** APM tools can provide support for OpenTelemetry data formats. As OpenTelemetry provides support for all telemetry signals - logs, metrics, and traces, it is possible for an APM tool to be based completely on OpenTelemetry. At SigNoz, we are building an OpenTelemetry native APM.

### How does AIOps fit in with OpenTelemetry?

**Pranay:** AIOps is applying advanced ML & AI algorithms to derive insights and help DevOps people maintain their systems more efficiently.

With the increasing adoption of OpenTelemetry, the format in which data is collected would be standardized. This would enable innovations like better out-of-the-box AI models which can work on OpenTelemetry data. The community can also publish pre-trained models for certain specific use cases like alerts.

We envisage this will open up more innovation in creating AI models which can work out of the box with OpenTelemetry data.

---

### Related Posts

[OpenTelemetry Collector - The Complete Guide](https://signoz.io/blog/opentelemetry-collector-complete-guide/)

[SigNoz - An OpenTelemetry native APM](https://signoz.io/blog/opentelemetry-apm/)