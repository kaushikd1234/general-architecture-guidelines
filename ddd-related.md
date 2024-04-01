#### Lambda Layer concept : https://docs.aws.amazon.com/lambda/latest/dg/chapter-layers.html


#### AWS Hands-On: Integrate AWS Step Functions with EventBridge

https://www.youtube.com/watch?v=f_uNbo2cunk&t=399s

https://github.com/CumulusCycles/AWS_Step_Functions_demo/tree/main?tab=readme-ov-file
#### My github demo project : https://github.com/kaushikd1234/aws-eventbridge-statemachine-demo/

#### Build a Serverless Workflow with AWS Step Functions

https://www.youtube.com/watch?v=DFSko_sLyMM

https://aws.amazon.com/step-functions/use-cases/#:~:text=In%20this%20example%2C%20you%20have,data%20is%20available%20in%20S3.



#### Exploring the Power of Event-Driven Architecture

https://blog.levelupcoding.com/p/luc-46-exploring-power-eventdriven-architecture


#### example code when hibernate update throws exception on update method

<img width="436" alt="image" src="https://github.com/kaushikd1234/general-architecture-guidelines/assets/123860112/07894629-2bac-4128-b002-132129481fb7">



#### Micro services design patterns 
https://microservices.io/patterns/apigateway.html

#### API composition and API aggegator pattern difference ?

**API Composition:**

Definition: API composition involves combining multiple APIs together to create a new, more comprehensive API that serves a specific purpose or functionality.

Purpose: The main goal of API composition is to simplify the consumption of APIs by providing a unified interface tailored to the needs of the application or service.

Implementation: In API composition, the integration logic is typically handled within the application itself. The application developer selects the necessary APIs and orchestrates them to achieve the desired functionality.

Example: Suppose you are building an e-commerce application. Instead of exposing separate endpoints for inventory management, payment processing, and shipping, you might compose these functionalities into a single API that handles the entire checkout process.

**API Aggregator:**

Definition: API aggregation involves collecting data or services from multiple APIs and presenting them to the user or application as a unified dataset or interface.

Purpose: The primary objective of API aggregation is to gather and consolidate information from disparate sources to provide a comprehensive view or service.

Implementation: In API aggregation, the integration logic is typically centralized within an aggregator service or layer. This aggregator service communicates with various APIs, retrieves data from them, and aggregates it before presenting it to the user or downstream applications.

**Example: Consider a weather application that displays weather forecasts from multiple sources (e.g., NOAA, AccuWeather, Weather.com). Instead of accessing each weather service individually, the application aggregates data from all sources and presents a single, unified forecast to the user.**

**Key Differences:**

Purpose: API composition focuses on combining APIs to create new functionality, while API aggregation focuses on gathering and presenting data or services from multiple APIs.

Implementation: API composition involves integrating APIs within the application itself, while API aggregation typically involves a centralized aggregator service or layer that communicates with multiple APIs.

Scope: API composition is more about designing APIs for specific use cases within an application, while API aggregation is about consolidating data or services from various sources into a single interface.

In summary, while both API composition and API aggregation involve integrating multiple APIs, they differ in their purpose, implementation, and scope. API composition creates new functionality by combining APIs within an application, while API aggregation gathers and presents data from multiple APIs in a unified manner


#### service mesh internal architecture 

The internal architecture of a service mesh typically involves several key components working together to facilitate communication between microservices. While specific implementations may vary, here's a general overview of the internal architecture of a service mesh:

**Data Plane**:

Sidecar Proxy: Each service instance is augmented with a sidecar proxy. This proxy is responsible for intercepting all inbound and outbound traffic to and from the service instance. It handles various tasks such as load balancing, routing, security, and telemetry collection.

**Control Plane:**

Service Discovery: This component keeps track of all available services and their instances within the mesh. It dynamically updates the service registry as new instances are deployed or existing instances are removed.

Traffic Management: This component is responsible for configuring routing rules and traffic policies within the service mesh. It enables features such as traffic splitting, A/B testing, canary deployments, and blue-green deployments.

Security: The security component manages policies and mechanisms for securing communication between services. This includes authentication, authorization, and encryption (e.g., mutual TLS) to ensure that only authorized services can communicate with each other securely.

Telemetry and Observability: This component collects telemetry data such as metrics, logs, and traces from the sidecar proxies to provide visibility into the behavior and performance of services within the mesh. It enables monitoring, troubleshooting, and performance optimization of microservices-based applications.

Configuration Management: This component centralizes the management of configuration settings for the service mesh. It allows operators to define and update configuration policies that govern the behavior of the mesh, such as routing rules, security policies, and traffic management policies.

**Overall, the internal architecture of a service mesh is designed to provide a dedicated infrastructure layer for managing communication between microservices in a distributed system. By decoupling communication concerns from individual services and centralizing them within the mesh, service meshes enable improved visibility, security, and reliability for microservices-based applications.**

#### What is SSL termination in AWS ALB ?
SSL termination in AWS Application Load Balancer (ALB) refers to the process of decrypting SSL/TLS encrypted traffic at the load balancer before forwarding it to the backend targets (such as EC2 instances or containers).

When SSL termination is enabled on an ALB, clients establish encrypted connections with the load balancer using HTTPS. The ALB then decrypts the incoming traffic, inspects the requests, and forwards them to the backend targets over the internal network in plain HTTP. This allows the backend targets to handle the requests without the overhead of SSL/TLS encryption and decryption.

SSL termination provides several benefits:

Offloading SSL/TLS Processing: By offloading SSL/TLS decryption to the load balancer, backend instances can focus on processing application logic without the overhead of SSL/TLS encryption and decryption. This can improve performance and reduce the computational load on backend instances.

Centralized Certificate Management: SSL termination allows for centralized management of SSL/TLS certificates at the load balancer level. Instead of deploying certificates on individual backend instances, certificates can be managed centrally on the load balancer, simplifying certificate management and ensuring consistency.

Improved Security: SSL termination allows the load balancer to inspect incoming traffic before forwarding it to backend instances. This enables the load balancer to perform security-related tasks such as access control, WAF (Web Application Firewall) filtering, and threat detection


#### difference between azure bridge and azure bus
#### Azure Service Bus:

Azure Service Bus is a fully managed enterprise integration message broker service, offering reliable message queuing and durable publish/subscribe messaging.
It enables communication between applications and services in a decoupled manner, allowing them to exchange messages asynchronously.
Key features include support for queues, topics, and subscriptions, as well as advanced messaging patterns like dead-lettering, sessions, and transactions.
Azure Service Bus is commonly used in scenarios such as application-to-application communication, event-driven architectures, and asynchronous workflows.
Azure Bridge:

#### Azure Bridge
this is a service designed specifically for bridging messaging between different messaging systems and protocols.
It acts as a connector between on-premises messaging systems and Azure messaging services, facilitating seamless communication between them.
Azure Bridge supports various messaging protocols like AMQP, MQTT, and MQ. It also supports different messaging systems such as IBM MQ, ActiveMQ, RabbitMQ, and more.
This service is particularly useful in hybrid cloud scenarios where organizations have existing on-premises messaging infrastructure and want to integrate it with Azure services without significant changes or disruptions.
In summary, while Azure Service Bus is primarily focused on providing messaging capabilities within Azure, Azure Bridge serves as a bridge between on-premises messaging systems and Azure services, facilitating interoperability and integration between different messaging environments.

#### Strangler fig pattern
https://docs.aws.amazon.com/prescriptive-guidance/latest/modernization-decomposing-monoliths/strangler-fig.html
#### Decompose by transactions
https://docs.aws.amazon.com/prescriptive-guidance/latest/modernization-decomposing-monoliths/decompose-transactions.html
#### decompose by domain example 
Decomposing a monolithic application by domain-driven design patterns involves breaking down the application into smaller, more manageable parts based on the distinct domains or business functions they serve. This approach helps in improving scalability, maintainability, and development agility. Here's a step-by-step guide to decompose a monolithic application by domain:

Identify Domains: Understand the various domains or business areas that the application serves. Domains could be related to user management, authentication, product catalog, order processing, billing, etc.

Analyze Dependencies: Analyze the dependencies between different components/modules within the monolith. Identify areas where there are tight couplings or where changes in one part of the application affect other parts.

Domain-Driven Design (DDD):

Bounded Contexts: Define bounded contexts for each domain. A bounded context is a specific boundary within which a particular domain model and its associated terminology apply. It helps in keeping the domain models isolated and focused.

Aggregate Roots: Within each bounded context, identify aggregate roots. An aggregate root is an entity that serves as a gateway to a group of related entities. It helps in maintaining consistency and transactional integrity within a domain.

Entities and Value Objects: Identify entities (objects with a distinct identity) and value objects (immutable objects without a distinct identity) within each domain.

Decompose by Microservices or Modules:

Microservices Approach: Decompose the monolith into microservices based on domain boundaries. Each microservice is responsible for a specific domain or subdomain.
Module Approach: If microservices are not feasible, decompose the monolith into modules based on domain boundaries. Each module encapsulates the logic related to a specific domain.
Define APIs and Contracts: Clearly define APIs and contracts between different modules or microservices. This ensures that communication between components is well-defined and loosely coupled.

Data Management:

Database Per Service: If using microservices, consider adopting a database per service approach where each microservice has its own database. This helps in maintaining data isolation and autonomy.

Shared Database with Schema per Service: If using modules within a monolith, consider maintaining a shared database but with separate schemas for each module/domain.
Implement and Refactor: Implement the decomposition strategy by creating new microservices/modules or refactoring existing codebase. Gradually migrate functionality from the monolith to the new architecture.

Testing and Deployment: Test each microservice/module independently to ensure its functionality. Implement continuous integration and deployment pipelines to automate the deployment process.

Monitoring and Management: Implement monitoring and management solutions to track the performance and health of each microservice/module. Use tools for logging, tracing, and monitoring to detect and diagnose issues.

Iterate and Improve: Continuously iterate on the architecture based on feedback and changing requirements. Refactor, optimize, and evolve the system over time to adapt to new business needs.

#### Domain-Driven Design (DDD)
this is an architectural approach and methodology for designing complex software systems based on a deep understanding of the business domain. It was introduced by Eric Evans in his book "Domain-Driven Design: Tackling Complexity in the Heart of Software." DDD emphasizes the importance of focusing on the core domain and modeling it explicitly within the software system.

Here are key concepts and principles of Domain-Driven Design:

Ubiquitous Language: DDD promotes the use of a common language, known as the ubiquitous language, shared by all members of the development team, including domain experts and developers. This language should reflect the domain concepts and terminology accurately, fostering better communication and understanding between technical and non-technical stakeholders.

Bounded Contexts: DDD divides a large, complex domain into smaller, more manageable bounded contexts. Each bounded context represents a cohesive area of the domain with its own explicit model and language. Boundaries are established to define where certain terms, concepts, and rules apply, ensuring consistency and clarity within each context.

Entity: An entity is a domain object with a unique identity that remains consistent over time. Entities encapsulate state and behavior relevant to the domain and are responsible for enforcing domain invariants.

Value Object: A value object is a domain object that represents a descriptive aspect of the domain with no conceptual identity. Value objects are immutable and defined solely by their attributes, making them interchangeable and easy to reason about.

Aggregate: An aggregate is a cluster of domain objects treated as a single unit. Aggregates define transactional consistency boundaries within the domain, ensuring that changes to the aggregate are enforced as a whole. Each aggregate has a root entity, known as the aggregate root, which serves as the entry point for accessing and modifying the aggregate's internal state.

Repository: Repositories provide a mechanism for accessing and persisting domain objects without exposing underlying data access details. Repositories abstract away the storage implementation, allowing domain objects to be retrieved and manipulated independently of the persistence mechanism.

Domain Events: Domain events represent significant state changes or business occurrences within the domain. They are used to capture and communicate meaningful events that have happened within the system. Domain events are typically immutable and can be used to trigger reactions or side effects in other parts of the system.

Context Mapping: Context mapping is the process of defining relationships and interactions between bounded contexts. It involves identifying integration points, sharing strategies, and establishing clear communication channels between different parts of the system.

Strategic Design: Strategic design focuses on aligning technical decisions with business goals and priorities. It involves making informed choices about where to invest resources, how to organize teams, and which architectural patterns to apply based on the strategic importance of different parts of the domain.

Overall, Domain-Driven Design encourages a collaborative approach to software development, where domain experts and developers work closely together to create a shared understanding of the business domain and translate that understanding into a well-designed software system. By focusing on the core domain, applying bounded contexts, and modeling domain concepts explicitly, DDD aims to tackle complexity and build software that reflects real-world business requirements effectively.

#### Ubiquitous Language example in DDD
In Domain-Driven Design (DDD), the concept of Ubiquitous Language refers to a common, shared language used by all members of a development team, including domain experts, developers, and stakeholders. This language is based on the domain model and is used to describe concepts, processes, and rules within the domain. By using the Ubiquitous Language consistently across all discussions, code, and documentation, DDD aims to ensure a clear and unambiguous understanding of the domain by all involved parties.

Here's an example of Ubiquitous Language in the context of an e-commerce application:

Domain: E-commerce

Ubiquitous Language:

Customer: A person who interacts with the e-commerce system to browse, purchase, and manage products.

Product: An item available for sale in the e-commerce store, characterized by attributes such as name, description, price, and availability.

Shopping Cart: A temporary container where customers can add products they intend to purchase before proceeding to checkout.

Order: A confirmed request made by a customer to purchase one or more products. It includes information such as the customer's details, the products being purchased, and the shipping address.

Checkout: The process of finalizing an order by providing payment and shipping information.

Inventory: The stock of available products in the e-commerce system. It tracks quantities, availability, and location of products.

Payment: The transfer of funds from the customer to the e-commerce system in exchange for products. It involves various payment methods such as credit cards, PayPal, or bank transfers.

Shipping: The process of delivering products from the e-commerce system to the customer's specified address. It includes options for shipping carriers, delivery speed, and tracking information.

### how to design solution for concurrent file processing swithout duplicate file processing in multiple nodes 

Designing a solution for concurrent file processing without duplicate processing across multiple nodes requires careful consideration of coordination, synchronization, and fault tolerance. Here's a comprehensive approach to designing such a solution:

File Ingestion and Distribution:

Implement a centralized or distributed file ingestion mechanism where files are evenly distributed across multiple nodes for processing. This could involve a load balancer or a distributed file system that evenly distributes files to processing nodes.
Unique File Identifiers:

Assign unique identifiers to each file at the point of ingestion. This identifier could be a combination of filename, timestamp, and any other metadata that ensures uniqueness.
Distributed Locking or Coordination:

Utilize a distributed coordination service like Apache ZooKeeper or etcd to manage distributed locks. Before processing a file, each node attempts to acquire a lock for that specific file. Only the node that successfully acquires the lock processes the file to ensure exclusive processing.
Idempotent Processing Logic:

Implement idempotent processing logic to handle cases where the same file might be processed multiple times due to failures or retries. Ensure that processing operations can be safely retried without causing duplicate side effects.
Checkpointing and Recovery:

Implement checkpointing mechanisms within your processing pipeline to keep track of processed files and their processing status. This helps in recovering from failures and resuming processing from the last checkpoint without reprocessing already processed files.
Monitoring and Alerting:

Set up monitoring and alerting systems to detect anomalies in file processing, such as unexpected duplicates or processing failures. Monitor the status of locks, processing queues, and processing nodes to ensure smooth operation.
Data Integrity Checks:

Perform data integrity checks during and after processing to verify that files have been processed correctly and no duplicates have been generated inadvertently. This could involve comparing processed data against expected outcomes or checksum validation.
Scalability and Load Balancing:

Ensure that the solution is scalable and can handle varying loads of file processing. Implement load balancing mechanisms to distribute processing tasks evenly across nodes and prevent overloading of any single node.
Retry and Backoff Strategies:

Implement retry and backoff strategies for processing tasks to handle transient failures gracefully. Retry failed processing tasks with exponential backoff to avoid overwhelming the system during periods of high contention or failures.
By incorporating these design considerations into your solution architecture, you can effectively handle concurrent file processing across multiple nodes without encountering issues related to duplicate processing.

### bean post processor snapshot and use
<img width="474" alt="image" src="https://github.com/kaushikd1234/general-architecture-guidelines/assets/123860112/d792af38-2b54-4c9d-8556-aa643adadc67">

#### sample youtube link 
https://www.youtube.com/watch?v=XfScG87YSHQ

#### enterprise integration patterns
https://www.enterpriseintegrationpatterns.com/patterns/messaging/
#### Spring Batch Dynamic File Upload Example | Spring Boot | JavaTechie
https://github.com/Java-Techie-jt/spring-batch-file-upload

#### spring batch version upgrade to springboot 3 my github account link
https://github.com/kaushikd1234/spring-batch-3-demo/tree/master



https://github.com/Java-Techie-jt/spring-batch-file-upload

