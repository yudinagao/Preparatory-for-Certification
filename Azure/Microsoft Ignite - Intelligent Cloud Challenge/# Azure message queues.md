# Azure message queues

- Service Bus queues - queuing, publish/subscribe and more advanced integration patterns. Integrate applications or components that may spam multiple communication protocols, data contracts, trust domains and network environments
- Storage queues - store large numbers of messages. You access message via HTTP, can bu up to 64Kb in size. Commonly used to create backlog  of work process asynchronously

## Choosing a queue solution

### Service Bus

- Without habing poll to queue
- FIFO
- Automatic Duplication detection
- Parallel long-running streams
- Transacional behavior and atomicity 
- Messages exceed 64 KB
- Queues - FIFO / Load Leveling send and receive with different rates
    - Receives: Receive and Delete / Peek Lock
- Topics and Subscriptions
- Messages carry a payload and metadata - Key-value and describes the payload
    - Broker properties: To, ReplyTo, ReplyToSessionID, MessageID, CorrelationId, SessionID


### Storage

- 80 GB of message in queue
- track process
- Require server side logs
- 