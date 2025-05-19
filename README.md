# End-to-End Deployment: Flask App with CI/CD and Docker

This guide walks through building, testing, and deploying a Flask application using Continuous Integration (CI) with Pytest and DockerHub.

## Table of Contents

- [Project Structure](#project-structure)
- [Setup](#setup)
- [Flask Application](#flask-application)
- [Testing with Pytest](#testing-with-pytest)
- [Continuous Integration](#continuous-integration)
- [Dockerization](#dockerization)
- [Deployment to DockerHub](#deployment-to-dockerhub)

---

## Project Structure

```
.
├── app.py
├── test_app.py
├── Dockerfile
├── requirements.txt
└── README.md
```

## Setup

1. **Clone the repository**
2. **Install dependencies**
    ```bash
    pip install -r requirements.txt
    ```

## Flask Application

- The Flask app is located in `app.py`.
- Example run:
  ```bash
  python app.py
  ```

## Testing with Pytest

- Tests are in the `test_app.py` file.
- Run tests:
  ```bash
  pytest test_app.py
  ```

## Continuous Integration

- Use GitHub Actions or similar CI tools.
- Example workflow:
  - Install dependencies
  - Run Pytest
  - Build Docker image if tests pass

## Dockerization

- Build Docker image:
  ```bash
  docker build -t yourusername/flask-app .
  ```
- Run container:
  ```bash
  docker run -p 5000:5000 yourusername/flask-app
  ```

## Deployment to DockerHub

1. **Login to DockerHub**
    ```bash
    docker login
    ```
2. **Push image**
    ```bash
    docker push yourusername/flask-app
    ```

---

## References

- [Flask Documentation](https://flask.palletsprojects.com/)
- [Pytest Documentation](https://docs.pytest.org/)
- [DockerHub](https://hub.docker.com/)
