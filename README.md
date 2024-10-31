# Flask CI App for test

This repository contains a sample Python Flask application integrated with a Continuous Integration (CI) pipeline using GitHub Actions. The CI pipeline includes build and test phases and can optionally build and publish a Docker image. Additionally, a Jenkins pipeline setup is provided for those who want to replicate the process using Jenkins.

## Features

- **Python Flask Application**: A simple web application that returns a message.
- **GitHub Actions CI Pipeline**:
  - **Build Phase**: Installs dependencies and prepares the application.
  - **Test Phase**: Runs unit tests to ensure the application works as expected.
- **Docker Support**:
  - Builds a Docker image for the Flask app.
  - Publishes the image to Docker Hub or any registry of choice.
- **Jenkins Pipeline** (Optional): Provides a `Jenkinsfile` for setting up a similar CI pipeline in Jenkins.

## Setup Instructions

### Prerequisites

- [Python 3.10+](https://www.python.org/)
- [Docker](https://www.docker.com/)
- [Git](https://git-scm.com/)

### Clone the Repository

```bash
git clone https://github.com/yourusername/flask-ci-app.git
cd flask-ci-app
