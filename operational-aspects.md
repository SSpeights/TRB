# Operational Aspects

In this section you cover all aspects for operating your software solution. Please answer the following general aspects in the beginning:

* How are incidents managed and communicated?
* What are the roles and responsibilities for operations? \(ownership model\)
* How are operating processes tied in with system development?

## Logging and monitoring {#OperationalAspects-Loggingandmonitoring}

One important cornerstone to have traceable and understandable operating for this solution is logging.

Please address the following checklist questions:

* How is logging implemented by the system?
* Do you use correlation ids that enable us to trace actions across the system landscape?
* Is there a federated log aggregation service in place?

## Availability {#OperationalAspects-Availability}

One cross-cutting aspect of delivering your application is guaranteeing a sufficient level of availability. This ranges from technical precautions such as redundant provisioning to manual processes. The goal of this subsection is to describe both the manual and technical aspects of delivering an available solution.

Related checklist questions:

* * What are the availability requirements for the systems / services? 
  * Which processes and mechanisms are in place to guarantee business continuity in case of emergency?
  * What technical mechanisms \(redundancy / automated failover / self-healing\) are used to improve the robustness and the availability of the software?
  * Are there watchdogs and automated mechanisms to cope with system failures?
  * Have you issued SLAs to your customers and how do you enforce them?
  * Do we rely on SLAs by external partners and software providers used by your software?
  * Are there backups required? If yes, how much / how often / which parts?

## Configurability {#OperationalAspects-Configurability}

A key challenge, especially for distributed solutions, is the management of system configurations. Please describe here how configurations are managed by / for your solution by addressing the following questions:

* How is the system / software / service configured?
* Is there a centralized configuration management solution?

## Maintainability {#OperationalAspects-Maintainability}

How do guarantee the maintainability of this software.

