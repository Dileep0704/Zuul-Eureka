1) Employee-service: A microservice that return emp details (running in 8011 port)
2) Micro-service2: A microservice has its endpoints and calls Employee-service in one endpoints (running in 8010 port)
3) Eureka-server: Eureka server registers all microservices (http://localhost:8761/)
4) Zuul: Api gateway, redirects the client requests to appropriate microservice. (running in 8662 port)


Ex: 

http://localhost:8662/service2/hello -> Zuul calls microservice2

http://localhost:8662/service2/employeeDetails/111 -> Zuul calls microservice2, where it internally calls employee service

http://localhost:8662/employee/findEmployeeDetails/222 -> Zuul calls employee service



reference: https://howtodoinjava.com/spring-cloud/microservices-monitoring/
https://medium.com/@iroshan.du/spring-boot-micro-services-with-eureka-and-zuul-proxy-with-fegin-client-68a3ad78453b

