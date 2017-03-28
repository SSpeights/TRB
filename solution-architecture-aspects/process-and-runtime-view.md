# Process and Runtime View

In contrast to the context view and the decomposition into building blocks, the process and runtime view explains "what is going on in/on your solution". Abstractly defined, it covers the behavior and interaction of the system’s building blocks as runtime elements \(processes, tasks, activities, threads …\). For example, if you're describing an integration platform of multiple services, here you would describe how these services interact and, for example, which messages are passed around by your solution.



* [Solution run-time processes](https://mywiki.grp.haufemg.com/display/HGTRB/Process+and+Runtime+View#ProcessandRuntimeView-Solutionrun-timeprocesses)
* [Deployment processes](https://mywiki.grp.haufemg.com/display/HGTRB/Process+and+Runtime+View#ProcessandRuntimeView-Deploymentprocesses)

## Solution run-time processes {#ProcessandRuntimeView-Solutionrun-timeprocesses}

The goal of this section is to describe functional processes supported by the solution. The main criterion for the choice of possible scenarios \(sequences, workflows\) is their relevancy. It is not important to describe a large number of scenarios. Please limit this section to a representative selection of processes. Candidates are:

* The top 3 – 5 use cases
* Solution startup
* The system’s behavior on its most important external interfaces
* The system’s behavior in the most important error situations

Your description should answer the following questions:

* * What are the main processes implemented by your solution?
  * How are these processes triggered?
  * How are the most important use cases executed by the solution components?
  * How does your solution co-operate with external and pre-existing components?
  * For software systems: Which instances of architectural building blocks are created at runtime and how are they started, controlled, and stopped.

## Deployment processes {#ProcessandRuntimeView-Deploymentprocesses}

Here you describe how you deploy your system / solution to its target environments. Your description should address the following TRB checklist questions:

* Where is the solution running? \(cloud-providers, hosting companies, on-premise applications\)
* What technologies are used to support the deployment processes?\(CI , CD\)
* How are the solutions "packaged" for shipping them to the run-time environment?\(Docker, WAR/EAR archives, .msi installer files...\)
* What needs to be done to carry out a baseline deployment on a bare environment?
* How are incremental deployments and updates carried out?
* What needs to be done to ship a hotfix?



