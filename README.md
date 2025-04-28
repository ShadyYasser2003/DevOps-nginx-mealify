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

![Successful Jenkins Pipeline](successful pipeline image.png)

This image shows a successful execution of the Jenkins pipeline for the Mealify project. It illustrates the different stages of the pipeline, including:

* **Start:** The beginning of the pipeline execution.
* **Checkout SCM:** Checking out the source code from the version control system (Git).
* **Build Image:** Building the Docker image for the Nginx application.
* **Trivy Vulnerability Scan:** Scanning the Docker image for potential security vulnerabilities.
* **Push Image:** Pushing the built Docker image to a container registry.
* **Deploy to k8s:** Deploying the application to the Kubernetes cluster (Minikube in this case).
* **Test NodePort Access:** Verifying that the application is accessible through the NodePort service.
* **End:** The successful completion of the pipeline.

The green checkmarks indicate that each stage of the pipeline was executed successfully. The "Test NodePort Access" section further confirms that the application is reachable.

## Docker Usage

Docker containerizes the Nginx web server along with the website content for consistent deployment.

## Kubernetes Deployment (Minikube)

Kubernetes manages the Nginx containers, ensuring scalability and availability.

## Git and GitHub Usage

Git handles version control, with GitHub as the remote repository for collaboration.