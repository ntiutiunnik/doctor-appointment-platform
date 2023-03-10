# Doctor appointment platform
Micro-service based Spring Cloud Project for doctor appointments deployed on Kubernetes IBM Cloud. 

## Architecture
The system consists of the following modules:

### Services
- **gateway-doctor-appointment** - Spring Cloud Gateway implementation of API Gateway pattern. Combines Swagger documentation of available services.
- **manager-doctor-appointment** - Main service with CRUD operations for managing doctor appointment platform.
- **manager-appointment-history** - Service which stores and aggregates appointment history.
- **dicovery-server** - Spring Cloud component used for service discovery.

### Databases
- **PostgreSQL** - Stores main entities for doctor appointment platform.
- **MongoDB** - Stores daily aggregation of appointment history.

### Event streaming
- **IBM Event Streams (Kafka)** - acts as a broker for appointment history publishing.

### Reverse Proxy
- **Ingress** - Kubernetes NGINX-based reverse proxy (Currently not supported on IBM Cloud free tier).

The following picture illustrates the IBM Cloud architecture described above.

![final schema (1)](https://user-images.githubusercontent.com/49955769/224269499-f50947ed-773f-4662-9b3e-1891ccc99011.jpg)

## Source code
https://github.com/ntiutiunnik/gateway-doctor-appointment

https://github.com/ntiutiunnik/manager-doctor-appointment

https://github.com/ntiutiunnik/manager-appointment-history

https://github.com/ntiutiunnik/discoveryserver

## Try it out
Swagger link for testing:
http://159.122.178.96:30339/swagger-ui/index.html

*WARN!* The link might expire due to IBM Cloud free tier policy
