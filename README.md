# Docker 

## [05 - Example Web Application](05-example-web-application/README.md)

Learning about containerization is interesting, but without a practical example it isn't very useful. In this section we create a 3 tier web application with a React front end client, two apis (node.js + golang), and a database. The application is as simple as possible while still providing a realistic microservice system to containerize.

## [06 - Building Container Images](06-building-container-images/README.md)

Demonstrates how to write Dockerfiles and build container images for the components of the example web app. Starting with a naive implementation, we then iterate towards a production ready container image.

## [07 - Container Registries](07-container-registries/README.md)

Explains what container registries are and how to use them to share and distribute container images.

## [08 - Running Containers](08-running-containers/README.md)

Using the containerized web application from sections 05 and 06, we craft the necessary commands to run our application with Docker and Docker Compose. We also cover the variety of runtime configuration options and when to use them.

## [09 - Container Security](09-container-security/README.md)

Highlights best practices for container image and container runtime security.

## [10 - Interacting with Docker Objects](10-interacting-with-docker-objects/README.md)

Describes how to use Docker to interact with containers, container images, volumes, and networks.

## [11 - Development Workflows](11-development-workflow/README.md)

Establishes tooling and configuration to enable improved developer experience when working with containers.

## [12 - Deploying Containers](12-deploying-containers/README.md)

Demonstrates deploying container applications to production using three different approaches: railway.app, a single node Docker Swarm, and a Kubernetes cluster.
