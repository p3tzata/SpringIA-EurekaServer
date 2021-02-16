Eureka Server:

mvn:spring-cloud-starter-netflix-eureka-server (Initializr:Eureka server )

@EnableEurekaServer in spring run main.

server.port=8761
eureka.instance.hostname=localhost
eureka.client.fetch-registry=false
eureka.client.register-with-eureka=false
eureka.client.service-url.defaultZone= http://${eureka.instance.hostname}:${server.port}/eureka
eureka.dashboard.path=/eurekaUI
#In production env must be eureka.server.enable-self-preservation=true 
eureka.server.enable-self-preservation=false 


Eureka Client:

spring-cloud-starter-netflix-eureka-client (Initializr:Eureka discovery client )
spring-boot-starter-web
		
eureka.client.service-url.defaultZone: http://localhost:8761/eureka
spring.application.name=eurekaClient_1


