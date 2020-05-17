## What is OpenEMP

OpenEMP is techincally a microservices web system serve to provide a set of tools and logical apps, so all together manage the education workflow.

OpenEMP is separated into components (service) that are completely isolated, services are meant to be highly configurable and independently deployable.

We so far have 4 types of services:

- **API Service**: a REST API web application that use JSON as a representation format
- **data Service**: responsible on storing data for an API service, this could be a SQL , NoSQL database, or a filesystem volume... 
- **UI Service**: is a frontend web application that fetch resources from API service and display a UI web component
- **System Service**: is a service that play a role in the orchestration between services, doesn't take part of the education model but ensure the data management across services

!!! note
    - data service can only communicate with one API service (it's a OneToOne relationship)


## Services Design

The following sketch is a demonstration of OpenEMP microservices:

![OpenEMP Microservice](/assets/images/sketch_microservices.jpg)

For more details about OpenEMP services, please check the services documentation [here](/services/index.md)