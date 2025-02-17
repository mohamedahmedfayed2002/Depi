# Kubernetes 3-Tier Application

This repository contains the necessary Kubernetes YAML files and configurations for deploying a 3-tier application consisting of a frontend, backend, and MySQL database.

## Project Structure

- `k8s/`: Contains all the Kubernetes YAML files for deployment, services, persistent volumes, and ingress.
  - `frontend-deployment.yaml`: Defines the deployment for the frontend.
  - `backend-deployment.yaml`: Defines the deployment for the backend.
  - `mysql-deployment.yaml`: Defines the deployment for MySQL with persistent storage.
  - `mysql-pv.yaml`: Persistent Volume for MySQL.
  - `mysql-pvc.yaml`: Persistent Volume Claim for MySQL.
  - `ingress.yaml`: NGINX Ingress for exposing the frontend.

## Steps I Followed

### 1. **Docker Images**
- Built Docker images for the frontend, backend, and MySQL.
- Pushed images to Docker Hub under `mo2002/frontend`, `mo2002/backend`, and `mo2002/mysql`.

### 2. **Kubernetes Configurations**
- Created Kubernetes deployment and service YAML files for the frontend, backend, and MySQL database.
- Configured Persistent Volumes (PV) and Persistent Volume Claims (PVC) for MySQL data.
- Exposed the frontend using an NGINX Ingress Controller.

### 3. **Deploying on Kubernetes**
- Applied the Kubernetes YAML files using `kubectl apply -f k8s/`.
- Verified the deployments with `kubectl get pods` and `kubectl get services`.

### 4. **Troubleshooting**
- Troubleshooted issues such as `ImagePullBackOff` and `Error` statuses in pods.
- Checked pod logs using `kubectl logs <pod-name>` to debug issues.

## To Run the Application Locally

1. Ensure Kubernetes is set up and running.
2. Apply the Kubernetes files using:
   ```sh
   kubectl apply -f k8s/
