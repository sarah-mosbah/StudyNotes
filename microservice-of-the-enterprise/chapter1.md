# The Case Of Microservice
- Microservices are services that deployed, scaled and devrloped indpendently.
## What's the proplem with Monolithic Apps:
- redeploy entire app.
- When things gets bigger it gets complex
- when things gets bigger IDE gets slower when you do testing for a feature.
- unstable service will bring app down 
- conflicting resource requirements. (For example, since a monolithic
application offers multiple business capabilities, one capability may
require more CPU while another requires more memory. It’s hard to
cater to the individual needs of these capabilities.

## service oriented architecture:
- Segregating functionalities to small service indepentent of each other "loosely coupled architecture", interfaces no concern about implementation

- Some common functionalities are written in the esb layer, like security and monitoring and business logic integration.
- The ESB 'E layer is a monolithic entity where
all developers share the same runtime to develop/deploy their service integrations.

## API
- is used to expose those web service functionalities
- The API layer is also used for security,
throttling, caching, and monetization.
- throttle means in simple defintion like a web server allowing only 10 users at a time 


### Microservice:
- Getting rid of ESB Layer by making service intercommunicate with other service

## Main Characterstics: 
### Business Capability Oriented:
- Service should do one thing in business and do it well.
### Autonomous: Develop, Deploy, and Scale Independently:
- Unlike web services or a monolithic application
architecture, services don’t share the same execution runtime. Rather they are deployed
as isolated runtimes by leveraging technologies such as containers.
- you can scale the microservice that needed to be scaled, the one with the biggest traffic, independently.

### Decentralized Data Management:
- each ms has its own database, so if you want to change one functionality schema it wont break rest of microservices
- no ms should be allowed to update any database except theirs.

## Benefits: 
- autonomous service development, no many cycles as in monolithic 'due to its size', focus on deployment functionality in the app not the whole app --> better in agile.

- Failure isolation --> service failure wont make the whole app fail.

- Ease of deployment and scaling

- give specific business functionality to a specific team to make its microservice

## Liabilities:
- inter-communication between microservice is more complicated, it took more time to create composite functionality.

- need to have a good monitoring and observing system to be able to detect failures.

- totally depends on containers
- databases transactions managment

# When to Use MS?
- When your app is complex
- When your app requires modularity


