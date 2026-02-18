In this project, I developed and deployed a fully functional web application using modern DevOps and cloud technologies. The project involved creating a simple web application with a frontend built using HTML, CSS, and JavaScript and a backend using Node.js (Express). Both components were containerized using Docker to ensure consistent and portable deployment.

The application was deployed on AWS, utilizing EC2 instances for hosting. Additionally, I implemented a CI/CD pipeline using GitHub Actions to automate the processes of building, testing, and deploying the application. 

Key achievements include successfully deploying Dockerized frontend and backend services on AWS, setting up robust CI/CD automation, and documenting the entire process with detailed instructions and deployment logs. This project provided hands-on experience with Docker, AWS services, and CI/CD workflows, equipping me with essential skills for modern software development and DevOps practices.





# MyWebApp
=======
# frontend-and-backend

![CI](https://github.com/wlsf82/frontend-and-backend/actions/workflows/ci.yml/badge.svg)

Sample project with basic "backend" and frontend, running Cypress tests on GitHub Actions.

## Pre-requirements

To run this project, you will need:

- [git](https://git-scm.com/downloads) (I've used version `2.34.1` while writing this doc)
- [Node.js](https://nodejs.org/en/) (I've used version `v18.15.0` while writing this doc)
- npm (I've used version `9.5.0` while writing this doc)

**Note:** When installing Node.js, npm is automatically installed too.

## Installing and starting the servers

Read the following [doc](./TestEnvironment.md) to install and start the backend and frontend servers.

## Installation of `devDependencies`

After cloning this project, to install the dev dependencies, run `npm install` (or `npm i` for short.)

## Tests

Run `npm run test:frontend:unit` to run the frontend unit tests.

Run `npm run test:api:with:servers` to run the API tests.

> **Note:** These scripts starts the required servers before-hand, and shuts them down when tests finish running.

Run `npm run test:frontend:with:server` to run the UI tests in headless mode.

> **Note 2:** This script starts the frontend server before-hand, and shuts it down when tests finish running.
>
> **Note 3:** When running in headless mode, if tests fail, Cypress automatically saves screenshots of the failures at `cypress/screenshots/`.

### Interactive mode

1. Run `npm run cy:open:with:servers` to open the Cypress Test Runner to run tests in interactive mode.

> **Note 4:** This script starts the required servers before-hand, and shuts them down after the runner is closed.

2. With the test runner opened, click on the test file you want to test.

__
