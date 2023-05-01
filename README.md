# Based on the following Microsoft Learn module

[https://github.com/MicrosoftDocs/mslearn-aks-workshop-ratings-web](https://github.com/MicrosoftDocs/mslearn-aks-workshop-ratings-web)

This code is part of the Microsoft Learn module of the AKS workshop. It provides the frontend for the ratings application.

## Contents

| File/folder       | Description                                |
|-------------------|--------------------------------------------|
| `src`             | Sample source code.                        |
| `static`          | Data and images.                           |
| `.gitignore`      | Define what to ignore at commit time.      |
| `.dockerignore`   | Define what to ignore at build time.       |
| `Dockerfile`      | Define how the Docker image is built.      |
| `README.md`       | This README file.                          |
| `LICENSE`         | The license for the sample.                |

## Prerequisites

To build this sample locally, you can either build using Docker, or using NPM.

- Install [Docker](https://www.docker.com/get-started)
- Install [NodeJS](https://nodejs.org/en/download/)

## Setup

- To build using Docker, in the project folder, run `docker build -t ratings-web .`
- To build using NPM, in the project folder, run `npm install`

## Running the sample

- To run using Docker, run `docker run -it -p 8080:8080 ratings-web`
- To run using NPM, run `npm start`

Required configuration via environment variables:

- API:  `<set to rating-api endpoint>`. This *does not* have to be publicly accessible. The application proxies the API requests via the backend to the rating-api endpoint.

The application exposes port 8080.
You should then be able to access the application at <http://localhost:8080>.