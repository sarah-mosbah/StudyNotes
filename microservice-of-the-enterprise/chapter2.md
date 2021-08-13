# Designing Microservices:

## DDD:
- each microservice belongs to specific domain, and be represented as domain.
- Each ms has its own way of communication structure to represent its business terminology.

- highlights the need to have a ubiquitous language to define the domain model. The ubiquitous language is a shared team language, which is shared by domain experts
and the developers. In fact, ubiquitous means that the same language must be used everywhere within a given context, from conversations to code.

## Bounded Context:
- it's what a domain model evolve around with all its language and keywords.
- domain could be represented by multiple microservices and multiple bounded context.

** Note: It is recommended that bounded contexts maintain their separation by each
having its own team, codebase, and the database schema.

- communication happened as event triggered from one ms to another and this called domain event  



-------------Revisit------------------------------