# Mealify.

## Technologies Used

* **Frontend:** HTML, CSS 
* **Web Server:** Nginx
* **Containerization:** Docker
* **Orchestration:** Kubernetes (Minikube for local development)
* **CI/CD:** Jenkins
* **Version Control:** Git
* **Repository:** GitHub

## Project Files Overview

* **`Jenkinsfile`:** Defines the CI/CD pipeline for automated builds and deployments using Jenkins.
* **`Dockerfile`:** Specifies the configuration for building the Docker image containing the Nginx web server and website files.
* **`deployment.yaml`:** Kubernetes configuration for deploying and managing the Nginx application.
* **`service.yaml`:** Kubernetes configuration for exposing the Nginx application within the cluster.
* **`nginx.conf`:** Configuration file for the Nginx web server.
* **`index.html` and `style.css`:** Core files for the website's structure and styling.
* **`images/`:** Directory containing the website's images.

## Local Setup and Execution (For Developers)

1.  **Prerequisites:** Git, Docker, Minikube, kubectl.
2.  **Clone Repository:** `git clone [repository-url]` and `cd [repository-name]`.
3.  **Build Docker Image:** `docker build -t [dockerhub-repo]:local .`.
4.  **Deploy with Minikube:** `kubectl apply -f deployment.yaml` and `kubectl apply -f service.yaml`. Access via `minikube service my-nginx-service --url`.

## Jenkins Pipeline

Jenkins automates the CI/CD process, including code checkout, Docker image building and pushing, and deployment to Minikube.

## Docker Usage

Docker containerizes the Nginx web server along with the website content for consistent deployment.

## Kubernetes Deployment (Minikube)

Kubernetes manages the Nginx containers, ensuring scalability and availability.

## Git and GitHub Usage

Git handles version control, with GitHub as the remote repository for collaboration.
