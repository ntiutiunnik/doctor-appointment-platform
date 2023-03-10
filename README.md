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

![final schema (2)](https://user-images.githubusercontent.com/49955769/224278956-282eccfb-a777-4948-8b0c-c43146b95e4e.jpg)

## Source code
https://github.com/ntiutiunnik/gateway-doctor-appointment

https://github.com/ntiutiunnik/manager-doctor-appointment

https://github.com/ntiutiunnik/manager-appointment-history

https://github.com/ntiutiunnik/discoveryserver

## Try it out
Swagger link for testing:
http://159.122.178.96:30339/swagger-ui/index.html

*WARN!* The link might expire due to IBM Cloud free tier policy
