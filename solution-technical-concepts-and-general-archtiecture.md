# Solution Technical Concepts and General Archtiecture

* [Persistency](https://mywiki.grp.haufemg.com/display/HGTRB/Solution%3A+Technical+Concepts+And+General+Architectural+Aspects#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Persistency)
* [User interface](https://mywiki.grp.haufemg.com/display/HGTRB/Solution%3A+Technical+Concepts+And+General+Architectural+Aspects#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Userinterface)

* [Transaction procession](https://mywiki.grp.haufemg.com/display/HGTRB/Solution%3A+Technical+Concepts+And+General+Architectural+Aspects#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Transactionprocession)
* [Session handling](https://mywiki.grp.haufemg.com/display/HGTRB/Solution%3A+Technical+Concepts+And+General+Architectural+Aspects#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Sessionhandling)
* [Exception / error handling](https://mywiki.grp.haufemg.com/display/HGTRB/Solution%3A+Technical+Concepts+And+General+Architectural+Aspects#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Exception/errorhandling)
* [Business rules](https://mywiki.grp.haufemg.com/display/HGTRB/Solution%3A+Technical+Concepts+And+General+Architectural+Aspects#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Businessrules)
* [Parallelization and threading](https://mywiki.grp.haufemg.com/display/HGTRB/Solution%3A+Technical+Concepts+And+General+Architectural+Aspects#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Parallelizationandthreading)
* [Internationalization](https://mywiki.grp.haufemg.com/display/HGTRB/Solution%3A+Technical+Concepts+And+General+Architectural+Aspects#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Internationalization)
* [Testability](https://mywiki.grp.haufemg.com/display/HGTRB/Solution%3A+Technical+Concepts+And+General+Architectural+Aspects#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Testability)
* [Plausibility and validity checks](https://mywiki.grp.haufemg.com/display/HGTRB/Solution%3A+Technical+Concepts+And+General+Architectural+Aspects#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Plausibilityandvaliditychecks)
* [Code generation](https://mywiki.grp.haufemg.com/display/HGTRB/Solution%3A+Technical+Concepts+And+General+Architectural+Aspects#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Codegeneration)
* [Build-management](https://mywiki.grp.haufemg.com/display/HGTRB/Solution%3A+Technical+Concepts+And+General+Architectural+Aspects#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Build-management)

The following chapters cover examples of frequent cross-cutting concerns or aspects.

Fill in these chapters if there is NO building block that covers these aspects. If some of the aspects are not relevant for your project mention this fact instead of removing the section.

# Persistency {#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Persistency}

Persistency means moving data from \(volatile\) memory to a durable storage medium \(and back\).

Some of the data that a software system is processing must be written to and read from persistent storage media.

* Volatile storage media \(main memory or cache\) are not designed for permanent storage. Data is lost if the hardware is switched off.
* The amount of data processed by commercial software systems normally exceeds the capacity of main memory.
* Hard disks, optical media and tapes often contain large amounts of existing business data that represent a significant investment.

Persistency is a technical issue that normally does not appear as part of the actual business functionality. An architect must deal with this issue nevertheless because most software systems require efficient access to persistently stored data. This is relevant for essentially all commercial and most technical systems; embedded systems on the other hand often differ in their data management requirements.

# User interface {#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Userinterface}

Software systems that are used interactively by \(human\) users require a user interface. These can be graphical, textual, or voice user interfaces.

# Transaction procession {#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Transactionprocession}

A transactions is a sets of operations or activities that must be processed either in its entirety or not at all. The term is especially relevant in the database area with the important notion of ACID-transactions \(atomic, consistent, isolated, durable\).

# Session handling {#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Sessionhandling}

A session identifies an active connection between a client and a server. The session state must be preserved, which is esp. important if stateless protocols such as HTTP are used for communications. Session handling is a critical challenge esp. for intra- and internet-systems and can strongly influence the performance of a system.

# Exception / error handling {#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Exception/errorhandling}

How are exceptions and errors handled systematically and consistently?

How can the system reach a consistent state after an error? Is this done automatically or is manual interaction required?This aspect is also related to logging and tracing,

Which kind of exceptions and errors are handled by the system? Which kind of errors are forwarded to which external interface and which are handled fully internally?

How are the exception handling mechanisms of your programming language used? Do you use checked or unchecked exceptions?

# Business rules {#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Businessrules}

How do you deal with business logic and business rules? Is business logic implemented in the corresponding business classes or is it handled in a central component? Do you use a rule engine for the interpretation of business rules \(production system, forward-/backward-chaining\)?

# Parallelization and threading {#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Parallelizationandthreading}

Applications can be executed in parallel processes or threads. This creates a need for synchronization points. The theory of parallel processing serves as a foundation for this aspect. The architecture and implementation of parallel systems needs to consider many technical details such as address spaces, applied mechanisms for synchronization – guards, semaphores, etc. – processes and threads, parallelism in the operating system, parallelism in virtual machines. etc.

# Internationalization {#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Internationalization}

This section covers support for usage of the system in different countries, i.e. adjusting the system to country specific attributes. Internationalization \(often abbreviated as “i18n” where “18” refers to the eighteen characters between the I and the n\) covers translation of text, usage of character encodings, display of fonts, writing of numbers and dates, and other \(external\) aspects.

# Testability {#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Testability}

Support for simple \(and if possible automated\) tests. This aspect is the basis for the important implementation pattern of “continuous integration”. Projects should support at least daily build-and-test cycles. Important keywords for this aspect are unit tests and mock objects.

# Plausibility and validity checks {#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Plausibilityandvaliditychecks}

How and where do you check plausibility and validity of \(input\) data, esp. user inputs?

# Code generation {#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Codegeneration}

How and where do you use code generators to create parts of the system from models or domain specific languages \(DSL’s\)?

# Build-management {#Solution:TechnicalConceptsAndGeneralArchitecturalAspects-Build-management}

How is the overall system created from is \(source code\) building blocks? Which repositories contain source code, where are configuration files, test cases, test data and build scripts \(make, ant, maven\) stored?

