# k8s-netgen

The objective of this repo is to create a k8s application that will generate microservice traffic for testing purpose.  Prefered would be the ability to generate traffic which can be collected and analized to determine if/what packets might have been lost.

Possible traffic generators might be fluent bit shipping to elastic search.  Another option is a golan application that listens for http requests. Each request calls X number of other microservices and responds back with success or the number of each microservice that failed to respond in the given time frame.

Test
