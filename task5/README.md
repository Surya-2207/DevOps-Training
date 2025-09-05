# Task 5: Kubernetes Deployment with Docker and YAML

## Overview
This task demonstrates how to deploy a web application using Kubernetes, Docker, and a YAML configuration file. The application consists of a simple HTML page and is managed using Kubernetes resources.

## Files
- `app.yml`: Kubernetes manifest file for deploying the web application.
- `index.html`: The web application's main HTML file.

## Steps

### 1. Build Docker Image
If you have a Dockerfile, build your image:
```powershell
# Example (replace <image-name> with your desired name)
docker build -t <image-name> .
```

### 2. Push Docker Image (Optional)
Push the image to a container registry if needed:
```powershell
docker tag <image-name> <your-registry>/<image-name>
docker push <your-registry>/<image-name>
```

### 3. Apply Kubernetes Manifest
Deploy the application using the provided YAML file:
```powershell
kubectl apply -f app.yml
```

### 4. Verify Deployment
Check the status of your deployment and service:
```powershell
kubectl get deployments
kubectl get services
```

### 5. Access the Application
Forward the service port to your local machine:
```powershell
kubectl port-forward svc/xops-web 8080:80
```
Then open [http://localhost:8080](http://localhost:8080) in your browser.

## Troubleshooting
- Ensure your Kubernetes cluster is running.
- Check pod logs for errors:
  ```powershell
  kubectl logs <pod-name>
  ```
- Restart deployment if needed:
  ```powershell
  kubectl rollout restart deployment xops-web
  ```

## Resources
- [Kubernetes Documentation](https://kubernetes.io/docs/)
- [Docker Documentation](https://docs.docker.com/)

---
**Author:** Surya-2207
