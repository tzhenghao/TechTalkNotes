Speaker: Martin Fowler
----------------------
https://www.youtube.com/watch?v=wgdBVIX9ifA

Monolith - scale by putting on multiple machines.


Microservices - put different services on different machines.

##Definition

Common Characteristics:

##Componentization via services

A component is:
independently replaceable
independently upgradeable

Service is running in its own process.

Inter process calls.

##Organized around business functions

Organize in between business functions instead - orders, shipping, catalog etc.

##Smart endpoints and dumb pipes

Good piping scheme, put intelligence in the endpoints.

##Decentralized Data Management

Talk to another service only via API

Languages and tools by different services and groups
Some use noSQL, yay freedom!

##Infrastructure Automation
Blue green deployment - mandatory
New boxes and spin them up

##Design for Failure
Distribute across nodes
Chaos Monkey to detect how resilient the network is.

##Are Microservices just SOA?
Microservices is a subset of SOA.

##How Big?
Responsibility is very flexible.

##What are the advantages?
Monolith - simple + familiar.
