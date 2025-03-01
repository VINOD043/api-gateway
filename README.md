# api-gateway
api-gateway

Reference: https://github.com/in28minutes/spring-microservices-v3/tree/main/04.docker

# Docker

## Images

- https://hub.docker.com/u/in28min
- Currency Exchange Service 
	- vinod043/mmv2-currency-exchange-service:0.0.1-SNAPSHOT
- Currency Conversion Service
	- vinod043/mmv2-currency-conversion-service:0.0.1-SNAPSHOT
- Eureka
	- vinod043/mmv2-naming-server:0.0.1-SNAPSHOT
- API GATEWAY
	- vinod043/mmv2-api-gateway:0.0.1-SNAPSHOT

## URLS

#### Currency Exchange Service
- http://localhost:8000/currency-exchange/from/USD/to/INR

#### Currency Conversion Service
- http://localhost:8100/currency-conversion/from/USD/to/INR/quantity/10
- http://localhost:8100/currency-conversion-feign/from/USD/to/INR/quantity/10

#### Eureka
- http://localhost:8761/

#### Zipkin
- http://localhost:9411/

#### API GATEWAY
- http://localhost:8765/currency-exchange/from/USD/to/INR
- http://localhost:8765/currency-conversion/from/USD/to/INR/quantity/10
- http://localhost:8765/currency-conversion-feign/from/USD/to/INR/quantity/10
- http://localhost:8765/currency-conversion-new/from/USD/to/INR/quantity/10

#### Commands
```
docker run -p 9411:9411 openzipkin/zipkin:2.23
docker push docker.io/vinod043/mmv2-currency-exchange-service:0.0.1-SNAPSHOT
docker-compose --version
docker-compose up
docker push vinod043/mmv2-naming-server:0.0.1-SNAPSHOT
docker push vinod043/mmv2-currency-conversion-service:0.0.1-SNAPSHOT
docker push vinod043/mmv2-api-gateway:0.0.1-SNAPSHOT
watch -n 0.1 curl http://localhost:8000/sample-api
```
