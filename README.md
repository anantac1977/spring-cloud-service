This is the application service component of the discovery server process.
 
In order to quickly bootstrap it, go to http://start.spring.io/ and use the Spring Initializr to stub it out.
Generate it with the dependencies Eureka Discovery, Devtools and the Actuator.

The annotation "@EnableDiscoveryClient" in the "ServiceApplication" class turns the service application into a client of the Discovery Server. This annotation basically, leads this service application to register itself with the Discovery server when it comes up. The value of the property "service.instance.name" is being passed as a program argument.

application.properties:

#Service name
spring.application.name=spring-cloud-service

#Discovery Server url
eureka.client.service-url.defaultZone=http://localhost:8761/eureka