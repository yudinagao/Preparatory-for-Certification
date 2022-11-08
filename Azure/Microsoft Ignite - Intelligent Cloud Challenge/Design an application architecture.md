# Design an application architecture

 - Communicate with each other effectively.
 - Be able to be deployed rapidly.
 - Be resilient when failures occur.
 - Be able to integrate with other systems seamlessly.

## Messages and Event scenarios

### Messages:
    - raw data
    - one to one
#### Queue Storage 

- Millions of messages
- Limited only by capacity of Azure Storage
- Securely accessed via REST-based interfae
- Realibility, garanteed message delivery and transactional support

#### Service Bus

- Support message queues and publish-subscribe topics
- Load-balance work
- Safely route and tranfer data and control 
- Coordinate transactional work that requires high degree of  reliability
- Better sed for High Value Enterprise messaging        

### Events:
    - lighter than messages
    - one to many

- Messages or Events or both
- Sender Expectations
- Guaranteed communication -> Messages
- Ephemeral Communication -> Events

|Messaging solution |	Example scenarios|
|-------            | ------             |
|Azure Queue Storage| 	You want a simple queue to organize messages.
You need an audit trail of all messages that pass through the queue.
You expect the queue storage to exceed 80 GB.
You'd like to track progress for processing a message inside of the queue.|
|Azure Service Bus message queues| 	You require an at-most-once delivery guarantee.
You require at-least-once message processing (PeekLock receive mode).
You require at-most-once message processing (ReceiveAndDelete receive mode).
You want to group messages into transactions.
You want to receive messages without polling the queue.
You need to handle messages larger than 64 KB but less than 256 KB.
You expect the queue storage won't exceed 80 GB.
You'd like to publish and consume batches of messages.|
|Azure Service Bus publish-subscribe topics| 	You need multiple receivers to handle each message.
You expect multiple destinations for a single message but need queue-like behavior.|

### Events Hubs Events

- Supports real time data ingestion
- Send and receive in differents languages or using apache storm
- Message received are added to end of the data stream
    - Data stream order messages according to time received
    - Consumers can seek data by using time offsets
- Pull model
    - hold each message in its cache and it's only read
    - when read, not deleted
- no build-in mechanism to handle message that aren't processed as expected
- Scales according to number of purchased throughput units
- scenarios: live dashboarding, analytics pipelines and anomalies life fraud or outlier actions
- consider language and framework integration
- Consider pricing  tier and throughput unit
- COnsider pull model benefits
- Consider message failures
- Consider data stream access
- Better used for Big Data Pipeline - Event Streaming
### Event Driven Solution

- Send and Forget Principle
- Azure Event Grid
    - Aggregates all of your events andd provides routing to any source to any destination
    - Handlers like Azure Functions or Azure DevOpsWebhooks
    - Source like Azure Blob Storage or Azure Media Service
    - Eliminates Subscribers - minimize cost and latency - no need for polling
    -  Better used for Reactvive Programming
    - Event Distribution - Discrete - React to status Change

## Caching Solutions

Caching: technique that aims to improve the performance and scalability of a system
    - Copies frequently accessed data to fast storage located close to applications
    - improves response time 
        - data store remains relatively static
        - slow compared to speed of the cache
        - high level of contention

### Azure Cache for Redis

Redis Open Source
Managed Servie of Redis labs

    - secure and dedicated Redis server instances and full Redis API compatibility
    - Distributed data or contenct cache, session store or message broker
    - Standalone or with others azure database services, like Azure SQL Server or Cosmos DB

|Pattern 	|Scenario 	|Solution|
|------     | ------    | -----  |
|Data cache | 	Databases are often too large to load directly into a cache.| 	It's common to use the cache-aside pattern to only load data into the cache as needed. When the system makes changes to the data, the system can also update the cache, which is then distributed to other clients. Additionally, the system can set an expiration on data, or use an eviction policy to trigger data updates into the cache.|
|Content cache 	|Many web pages are generated from templates that use static content such as headers, footers, banners. These static items shouldn't change often. 	|Using an in-memory cache provides quick access to static content compared to back-end datastores. This pattern reduces processing time and server load and allows web servers to be more responsive. A content cache can allow you to reduce the number of servers needed to handle loads. Azure Cache for Redis provides the Redis Output Cache Provider to support this pattern with ASP.NET.|
|Session store 	|A session store is commonly used with shopping carts and other user history data that a web application might associate with user cookies. Storing too much in a cookie can have a negative effect on performance as the cookie size grows and is passed and validated with every request. 	|A typical solution uses the cookie as a key to query the data in a database. It's faster to use an in-memory cache like Azure Cache for Redis to associate information with a user than interacting with a full relational database.|
|Job and message queuing 	|Some application operations take significant time to complete, which might prevent other unrelated jobs or messages from starting. 	|Applications often add tasks to a queue when the operations associated with the request take time to execute. Longer running operations are queued to be processed in sequence, often by another server. This method of deferring work is called task queuing. Azure Cache for Redis provides a distributed queue to enable this pattern in your application.|
|Distributed transactions 	|Applications sometimes require a series of commands against a back-end datastore to execute as a single atomic operation. All commands must succeed, or all commands must be rolled back to the initial state. 	Azure Cache for Redis supports executing a batch of commands as a single transaction.|

## API Integration

### Azure API Management

- publish, secure, maintain and analyze
- Consider number of API's
- Consider rate of API Changes
- Consider API administration load
- Consider Standardizing disparate API
- Consider Centralized API Management
- Consider enhanced API security

## Automated App Deployment

### Azure Resource Manager Template

- Idempotent
- Deployment in parallel
- Preview changes with WhatIf Statement
- VAlidation of templates before deployment process
- Break templates into smaller components and link them at deployment
- Integrate CI/CD like Azure DevOps and GitHub Actions
- bash or PowerShell within Templates
- JSON or Bicep
    - Bicep is Azure native

### Azure Automation

#### Process Automation
Automate frequent, time-consuming, and error-prone cloud management tasks
#### Configuration Management
The service supports change tracking across services, daemons, software, registry, and files in your environment. The change tracking helps you diagnose unwanted changes and raise alerts.
#### Update Management
create scheduled deployments that orchestrate the installation of updates within a defined maintenance window.

### App Configuration Management

#### Azure App Configuration

- fully managed and support natie integration with popular frameworks
- flexible keys representations and mapping and point-in-time replay of settings
- Dedicated UI for flag management and resource tagging with labels
- Compare two sets of configuration
- Enhanced security through Azure Active Directory
- Sensitive information can be encrypted at rest and in transit.
- Work in development and production environments
