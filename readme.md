# Mavie Customer Backend API

This repository contains the OpenAPI specifications for the Mavie Customer Backend API. It includes YAML files defining the API paths, components, and responses.

## Getting Started

These instructions will guide you through setting up the project on your local machine for development and testing purposes.

### Prerequisites

- [Node.js and npm](https://nodejs.org/en/download/)
- [Docker](https://www.docker.com/products/docker-desktop) (optional, for running Swagger UI locally)
- Git (for cloning the Swagger UI repository)

### Running the Swagger-CLI Bundle

To compile the OpenAPI specifications into a single bundled file, you can use the `swagger-cli` tool. First, install `swagger-cli` globally using npm:

```bash
npm install -g swagger-cli
```
Then, run the following command in the root directory of this repository to bundle the API specifications:
```bash
swagger-cli bundle -o mavie.yml api-spec.yml
```
This command will generate a bundled file named mavie.yml.

### Viewing the API Specification

#### Using an Online Editor

You can view and interact with the API specification using the Swagger Editor online. Simply go to [Swagger Editor](https://editor.swagger.io), and import the bundled API specification file (`mavie.yml`).

#### Running Swagger UI Locally with Docker

To run Swagger UI locally using Docker, execute the following command:

```bash
docker run -p 80:8080 -e SWAGGER_JSON=/foo/bundled-api-spec.yml -v $(pwd):/foo swaggerapi/swagger-ui
```
This command will start a Swagger UI instance running on http://localhost. You can view your API documentation by navigating to this URL in your web browser.

Running Swagger UI by Cloning the GitHub Repository
Alternatively, you can clone the Swagger UI GitHub repository and run it locally:
```bash
git clone https://github.com/swagger-api/swagger-ui.git
cd swagger-ui
npm install
npm run dev
```
After running these commands, Swagger UI will be available at localhost (localhost:80 for docker)
