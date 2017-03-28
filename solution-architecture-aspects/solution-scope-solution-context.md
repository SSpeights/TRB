# Solution Scope / Solution Context

The goal of this section is to explain how a solution \(for example a new service\) is embedded in the Haufe ecosystem.

* Identify all neighboring systems and specify all logical / business data that is exchanged with the system under development.
* Use a System Context Diagram to represent all external entities that may interact with your solution.
* Add data formats and communication protocols with neighboring systems and the general environment if these are not specified in detail with the relevant components.



It's best to use a separate list to add details about the relation to neighboring systems like

data formats, communication protocols etc.

## Solution context diagram {#SolutionScope/SolutionContext-Solutioncontextdiagram}

Use a System Context Diagram to represent all external entities that may interact with your solution. Such a diagram pictures the solution at the center, with no details of its interior structure, surrounded by all its interacting systems and services, environments and activities. The objective of the system context diagram is to focus attention on external factors and events that should be considered in developing a complete set of systems requirements and constraints.

You will answer the following questions here:

* How are they embedded into the haufe ecosystem? Show a context diagram!
* What are the main building blocks / components/\(microservices\) developed by the project?
* Which internal and external services / APIs \(outside Haufe\) are used?

## Interaction list {#SolutionScope/SolutionContext-Interactionlist}

The Interaction List lists all communication endpoints provided and used by your solution.

This enables you / us to answer the following questions:

* Which internal and external services/APIs \(outside Haufe\) are used? 
* Which kind of interfaces between the components and services are used? 
* Which technologies \(REST, RPC, SOAP\) and which dataformats \(JSON, XML...\) are used fore each interface?



