ABBA Whitepaper
Abstract
The ABBA whitepaper outlines a comprehensive solution for each foundational principle, designed to leverage the Erlang Virtual Machine (Beam) for creating resilient and scalable systems. These principles focus on utilizing Beam's process model through agent-centric design, achieving modularization within a monolithic framework for simplified operational management, and facilitating direct communication via function calls to minimize latency. It also emphasizes the orchestration of agents for a serverless-like experience and the use of predefined building blocks like Mnesia, PostgreSQL, Phoenix, and Nx for enhanced developer productivity. The whitepaper details how ABBA's innovative message bus architecture, integration of UBF with potential Protobuf support for efficient data serialization, and dynamic discovery mechanisms contribute to its goals of scalability, resilience, and operational simplicity, showcasing practical applications and benefits across various domains.




Protocols
ABBA defines the following protocols.
Whisper Protocol for Service Discovery
Facilitates dynamic service discovery across distributed systems, allowing services to discover each other without a centralized registry. Used by connected ABBA nodes to tell other nodes in the network which services are available. The ABBA system uses this protocol internally.
Local Service Discovery through mDNS
Enables services on the same local network to discover each other, which is useful for environments where services are closely located. The ABBA system uses this protocol internally.


ABBA Service Discovery Protocol
A higher-level protocol that utilizes both Whisper and mDNS for robust service discovery across various environments. This is the protocol used by applications or services to discover each other.

Protocol for Defining Versions and APIs: Ensures that services can define and expose their APIs and versions, supporting direct function calls, ABBA service calls, and REST calls based on proximity and implementation.

ABBA Message Bus Protocol
Addresses the messaging infrastructure within ABBA, including addressing and authentication, to secure and streamline communication between services.

Protocol Definition for UBF and Protobuf
Underpins the data protocol within ABBA, leveraging UBF for universal binary format and extending support to Protobuf for efficient data serialization.

These protocols ensure that the ABBA framework supports scalable, resilient, and efficient communication and data exchange across distributed systems while facilitating ease of development and deployment.
ABBA Services
ABBA Message Bus
A core communication platform for efficient, secure message exchange across services.
Service Registry: A dynamic directory for service discovery, enabling services to register and locate each other.
Service Monitor
Tools for monitoring, logging, and debugging agents, enhancing observability and operational insight.
API Utilities
This includes a functional API to message service API utility and one for REST, facilitating seamless service interactions.
Orchestration
Manages service coordination across and within nodes, ensuring optimal resource utilization and task execution.
Zero-touch Deployment
Simplifies service deployment, automating the provisioning and setup process.
Predefined Interfaces
For key technologies like Mnesia, PostgreSQL, Phoenix, and Nx, enabling automatic configuration and startup.

Seamless Integration
Ensures tight coupling between service APIs and the ABBA message bus for coherent communication flows.

