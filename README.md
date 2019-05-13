# Interview Notes

## Spring

### Spring Boot

* Bootstrap an application with zero or minimal configuration
* Heavy use of annotations and dependencies detection (auto-configuration) 

### Spring Cloud

* Configuration is versioned and distributed (config server)
* Service discovery and registration (Eureka)
* Service requests (Feign client)
* Gateway and routing (Zuul)
* Circuit breaker (Hystrix)
* Client side load balancing (Ribbon)
* Monitoring
* Advanced Message Queuing Protocol (Spring AMQP)

## Microservices architecture

### Advantages

* Smaller code base which is independent
* Scalled and deployed individually
* Avoid single point of failure on service or instance
* Allow the use of different tech stacks

### Disadvantages

* Distributed architecture is complex
* Networks calls increase delays and failures
* Increased effort due to multiple configurations and deployables
* Transaction safety (ACID) is hard to achieve

### Handling transactions

1. Avoid transactions (split data)
2. Two-Phase Commit Protocol (2PC)
   * Prepare phase
   * Commit phase (synchronous with commit/abort)
3. Eventual Consistency: Saga pattern
   * Asynchronous
   * Event bus
   * Compensation if error
