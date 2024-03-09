#### Microservices Architecture 
a collection of small independent services. self contained units - communication with other services via API, HTTP or Message Queues. 

- Enables horizontal scalability 
- Independent Deployment 

##### Challenges 
- Ensure reliable inter-service communication and maintaining data consistency. 
- Implement robust fault tolerance mechanisms and handling communication failures. 
- service discovery, monitoring, logging mechanisms, and latency considerations. 

#### Design Patterns

- Service Autonomy 
- Bounded Contexts 
- Decentralized Governance 

#### Service Discovery 
- Service Discovery Patterns facilitate dynamic service registeration and discovery, allowing services to find and connect without hardcoded dependencies. 


#### Cicuit Breaker
If the service becomes unresponsive or experience errors, the circuit breaker trips and routes requests to an alternative path, such as a fallback service or cached data. 

#### API Gateway
provides a central entry point for clients to access the microservices. It serves as an intermediary between the clients and the underlying services, abstracting the complexities of service communication and providing an unified API. 