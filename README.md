# Serverless Service Alternatives Report
*CST8917 – Serverless Applications - Assignment 2*

- Student Name: Rahaf Alkhlaf
- Student Username: alkh0115

## Introduction 
Throughout the course, we have developed and deployed applications using various Microsoft Azure serverless services. 
The purpose of this report is to expand our cloud knowledge by identifying equivalent services provided by **Amazon Web Services (AWS)** and **Google Cloud Platform (GCP)** for each Azure serverless service studied.

The report provides:
- A brief overview of each Azure service and its AWS/GCP equivalents.
- A comparison of **core features**, **integration options**, **monitoring & observability tools**, and **pricing models**.
- Strengths and weaknesses of each service from a **serverless architecture perspective**.

## Azure vs. AWS vs. GCP – Serverless Service Comparisons

### 1. Azure Functions (Triggers & Bindings)
| Cloud Provider | Service Name | Overview |
| --- | --- | --- |
| **Azure** | Azure Functions | Event-driven, serverless compute that runs code in response to triggers. Supports multiple languages and bindings for integration. |
| **AWS** | AWS Lambda | Serverless compute service that runs code in response to events from AWS services or HTTP requests. |
| **GCP** | Cloud Functions | Event-driven serverless compute platform supporting HTTP, Cloud Storage, Pub/Sub, and more. |

**Core Features**
- **Azure Functions**: Timer, HTTP, Blob, Queue, Event Grid, Service Bus triggers/bindings.
- **AWS Lambda**: API Gateway, S3, DynamoDB, SNS/SQS, CloudWatch events.
- **GCP Cloud Functions**: HTTP, Cloud Storage, Pub/Sub, Firebase, Cloud Scheduler.

**Integration Options**
- Azure: Azure DevOps, GitHub Actions, Event Grid, Logic Apps.
- AWS: CodePipeline, EventBridge, Step Functions.
- GCP: Cloud Build, Pub/Sub, Workflows.

**Monitoring & Observability**
- Azure: Azure Monitor, Application Insights.
- AWS: CloudWatch, X-Ray.
- GCP: Cloud Monitoring, Cloud Trace, Cloud Logging.

**Pricing Model**
- Pay-per-execution (millions of requests free tier).
- Charged by execution time and memory consumption.

**Strengths & Weaknesses**
- Azure: Strong bindings ecosystem, easy integration with Azure services.
- AWS: Broadest event source coverage, mature ecosystem.
- GCP: Simple setup but fewer native trigger types.

---

### 2. Durable Functions (Chaining, Orchestration, Fan-out/Fan-in)
| Cloud Provider | Service Name | Overview |
| --- | --- | --- |
| **Azure** | Durable Functions | Extension of Azure Functions enabling stateful workflows with patterns like chaining and fan-out/fan-in. |
| **AWS** | AWS Step Functions | Visual workflow orchestration service for coordinating AWS services. |
| **GCP** | Workflows | Orchestration service for connecting HTTP-based services and APIs in a serverless manner. |

**Core Features**
- Orchestration, state management, long-running workflows.
- Support for chaining, fan-out/fan-in, and human interaction patterns.

**Integration Options**
- Azure: Logic Apps, Service Bus, Event Grid.
- AWS: Lambda, SQS, SNS, DynamoDB.
- GCP: Cloud Functions, Pub/Sub, Cloud Run.

**Monitoring & Observability**
- Azure: Application Insights, Azure Monitor.
- AWS: CloudWatch metrics and execution history.
- GCP: Cloud Logging, Cloud Trace.

**Pricing Model**
- Based on number of state transitions and execution time.

**Strengths & Weaknesses**
- Azure: Code-based orchestration, deeply integrated with Azure Functions.
- AWS: Strong visual workflow design, robust service integrations.
- GCP: Lightweight but integrates well with HTTP-based APIs.

---

### 3. Azure Logic Apps
| Cloud Provider | Service Name | Overview |
| --- | --- | --- |
| **Azure** | Logic Apps | Workflow automation and integration platform with connectors for 300+ services. |
| **AWS** | AWS Step Functions (Express Workflows) | Orchestration with support for fast, high-volume event processing. |
| **GCP** | Workflows | Orchestration connecting GCP services and external APIs. |

**Core Features**
- Pre-built connectors for SaaS and enterprise applications.
- Visual designer for workflows.
- Event-driven and scheduled triggers.

**Integration Options**
- Azure: Power Automate, Functions, API Management.
- AWS: Lambda, API Gateway, EventBridge.
- GCP: Cloud Functions, Cloud Tasks.

**Monitoring & Observability**
- Azure: Azure Monitor, Log Analytics.
- AWS: CloudWatch metrics and logging.
- GCP: Cloud Monitoring.

**Pricing Model**
- Per action/connector execution.

**Strengths & Weaknesses**
- Azure: Richest connector library.
- AWS: Integrated with AWS services but fewer SaaS connectors.
- GCP: Strong API integration but limited pre-built connectors.

---

### 4. Azure Service Bus (Queues & Topics)
| Cloud Provider | Service Name | Overview |
| --- | --- | --- |
| **Azure** | Service Bus | Enterprise message broker supporting queues and publish/subscribe topics. |
| **AWS** | Amazon SQS (Queues) / Amazon SNS (Topics) | Managed messaging services for queue-based and pub/sub messaging. |
| **GCP** | Pub/Sub | Global messaging service for asynchronous event-driven communication. |

**Core Features**
- Azure: FIFO and non-FIFO queues, topics, sessions, dead-lettering.
- AWS: SQS for queues, SNS for pub/sub.
- GCP: Pub/Sub topics/subscriptions.

**Integration Options**
- Azure: Functions, Logic Apps, Event Grid.
- AWS: Lambda, Step Functions.
- GCP: Cloud Functions, Dataflow.

**Monitoring & Observability**
- Azure: Azure Monitor, Service Bus Explorer.
- AWS: CloudWatch metrics, logging.
- GCP: Cloud Monitoring.

**Pricing Model**
- Per operation, message size, and retention.

**Strengths & Weaknesses**
- Azure: Strong hybrid support, rich messaging features.
- AWS: Reliable and scalable but requires combining SQS and SNS.
- GCP: Simple, global service but fewer advanced queue features.

---

### 5. Azure Event Grid
| Cloud Provider | Service Name | Overview |
| --- | --- | --- |
| **Azure** | Event Grid | Event routing service supporting custom and system events. |
| **AWS** | EventBridge | Serverless event bus for routing events from AWS services and custom sources. |
| **GCP** | Eventarc | Event routing from GCP services, SaaS, and custom sources. |

**Core Features**
- Event filtering, delivery retries, multiple destinations.

**Integration Options**
- Azure: Functions, Logic Apps, Service Bus.
- AWS: Lambda, Step Functions.
- GCP: Cloud Functions, Workflows.

**Monitoring & Observability**
- Azure: Azure Monitor, diagnostics logs.
- AWS: CloudWatch metrics and event replay.
- GCP: Cloud Logging.

**Pricing Model**
- Per event published/delivered.

**Strengths & Weaknesses**
- Azure: Rich built-in event sources.
- AWS: Tight integration with AWS ecosystem.
- GCP: Integrated with GCP services but newer than others.

---

### 6. Azure Event Hubs
| Cloud Provider | Service Name | Overview |
| --- | --- | --- |
| **Azure** | Event Hubs | Big data streaming platform and event ingestion service. |
| **AWS** | Kinesis Data Streams | Scalable real-time data streaming service. |
| **GCP** | Pub/Sub | Real-time messaging and streaming ingestion. |

**Core Features**
- High throughput event ingestion, partitioned consumers, retention policies.

**Integration Options**
- Azure: Stream Analytics, Functions.
- AWS: Lambda, Firehose.
- GCP: Dataflow, Cloud Functions.

**Monitoring & Observability**
- Azure: Azure Monitor, diagnostic metrics.
- AWS: CloudWatch.
- GCP: Cloud Monitoring.

**Pricing Model**
- Based on throughput units and retention.

**Strengths & Weaknesses**
- Azure: Strong Azure ecosystem integration.
- AWS: Advanced analytics with Kinesis ecosystem.
- GCP: Simpler pricing, global availability.

---
## References

- Amazon Web Services. (n.d.). *What is Amazon Kinesis Data Streams?*. Retrieved from https://docs.aws.amazon.com/streams/latest/dev/introduction.html  
- Amazon Web Services. (n.d.). *What is AWS Step Functions?*. Retrieved from https://docs.aws.amazon.com/step-functions/latest/dg/welcome.html  
- Amazon Web Services. (2025, August 4). *What is Amazon SQS?*. Retrieved from https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html  
- Amazon Web Services. (2025, August 5). *What is Amazon EventBridge?*. Retrieved from https://docs.aws.amazon.com/eventbridge/latest/userguide/what-is-amazon-eventbridge.html  
- Amazon Web Services. (2025, August 7). *What is AWS Lambda?*. Retrieved from https://docs.aws.amazon.com/lambda/latest/dg/welcome.html  
- Amazon Web Services. (2025, July 22). *What is Amazon SNS?*. Retrieved from https://docs.aws.amazon.com/sns/latest/dg/welcome.html  
- Google Cloud. (2025, August 7). *What is Cloud Pub/Sub?*. Retrieved from https://cloud.google.com/pubsub/docs/overview  
- Google Cloud. (2025, August 7). *What is Eventarc?*. Retrieved from https://cloud.google.com/eventarc/docs/overview  
- Google Cloud. (2025, August 7). *What is Workflows?*. Retrieved from https://cloud.google.com/workflows/docs/overview  
- Google Cloud. (2025, August 7). *When should I deploy a function to Cloud Run?*. Retrieved from https://cloud.google.com/run/docs/functions-with-run  
- Microsoft. (2025, January 29). *What is Azure Logic Apps?*. Retrieved from https://learn.microsoft.com/en-us/azure/logic-apps/logic-apps-overview  
- Microsoft. (2025, March 13). *What is Azure Service Bus?*. Retrieved from https://learn.microsoft.com/en-us/azure/service-bus-messaging/service-bus-messaging-overview  
- Microsoft. (2025, March 25). *What is Azure Functions?*. Retrieved from https://learn.microsoft.com/en-us/azure/azure-functions/functions-overview  
- Microsoft. (2025, April 6). *What is Durable Functions?*. Retrieved from https://learn.microsoft.com/en-us/azure/azure-functions/durable/durable-functions-overview  
- Microsoft. (2025, August 7). *What is Azure Event Grid?*. Retrieved from https://learn.microsoft.com/en-us/azure/event-grid/overview  
- Microsoft. (2025, December 17). *What is Azure Event Hubs?*. Retrieved from https://learn.microsoft.com/en-us/azure/event-hubs/event-hubs-about  

