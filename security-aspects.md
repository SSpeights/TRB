# Security Aspects

This chapter documents all relevant aspects related to solution security. Here, we distinguish between network security, system / solution security, application security and data protection. Please clarify also who is responsible for threat analysis, protection requirements, etc. and security audits.

## Network security {#SecurityAspects-Networksecurity}

This section describes all tactics and actions you take to secure the networking context of your solution.

* What mechanisms are used to guarantee network security? \(Firewall, VLANs, DMZ, rule sets , DDOS\)
* Does a central identity management exist? If yes, which base and standards are supported \(OpenID / OAuth / Step2 / Keberos / etc.\)

## Solution and system security {#SecurityAspects-Solutionandsystemsecurity}

Here you describe your security analyses and the analysis-based mechanisms to secure this software solution. Please address the following questions:

* What are the most important and probable attacker scenarios? What is being done to protect the system against them?
* Provide a brief description of the role and authorization concept on the system level
* What actions \(for example hardening\) have been taken to protect the system against tampering? \(best practice system setup\)

## Application and development security {#SecurityAspects-Applicationanddevelopmentsecurity}

Here you'll explain how you treat security in the software realization process. Also describe which actions you take in order to harden your solution against common attack patterns \(Cross-Site-Scripting, SQL-Injections, XSRF...\)

Please provide answers to the following questions \(where applicable\)

* * * Are the secure development guidelines being applied?
      Link
    * Is there any analysis of potential attack scenarios of the software?
    * Is there any static-code analysis \(Fortify, Findbugs\) to assess common issues?
    * Are there any pentests or reviews to figure out how the software can be vulnerated?
    * Are there special precautions to protect the application against a\) cross-site scripting, b\)cross-site request forgery and c\) sql-injection attacks?
    * Do you encrypt data at rest and in transit? If yes, how?
    * How do you manage credentials and authorization\(oauth, saml2, oidc\)?



## Data protection {#SecurityAspects-Dataprotection}

Here you will describe different aspects to data protection and privacy. Please refer to the following checklist questions:

* * * How do you implement data protection class grouping?
      Link auf Matrix 
    * Identify the data which has to be processed, stored and transmitted. Give a data summary.
    * Are you clear on all data processing activities and their BDSG implications ? \(inside or outside application boundaries\)
    * Are special certifications required? \(ISO/IEC 27001, PCI DSS, FISMA , HIPAA…\)
    * Is the customer's consent to BDSG § 4a necessary for processing / storing the data ?



