# Online Book Reader

## Reader.Web

- Hosted as Azure App Service
- Hosted in multi-region
- Backed by Microservices
- Communicates with Azure App Gateway with Azure API Management listener
- APIs from Microservices are imported into Azure API Management - using OpenAPI specification
- Azure Front-Door as Layer-7 load balancer