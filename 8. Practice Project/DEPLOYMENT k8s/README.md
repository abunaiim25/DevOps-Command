# Laravel eCommerce Kubernetes Deployment

This repo contains Kubernetes manifests to run a Laravel app with MySQL and Redis.

## Quick start
1. Replace `your-docker-repo/laravel-app:latest` with your real image tag in files.
2. Save files into the folder structure shown.
3. Apply manifests (recommended order):

kubectl apply -f DEPLOYMENT/RBAC/
kubectl apply -f DEPLOYMENT/database/
kubectl apply -f DEPLOYMENT/redis/
kubectl apply -f DEPLOYMENT/laravel-app/
kubectl apply -f DEPLOYMENT/custom-resource/
kubectl apply -f DEPLOYMENT/jobs/
kubectl apply -f DEPLOYMENT/network/

4. To test locally:
kubectl port-forward svc/laravel-app 8080:80
then open http://localhost:8080

5. Jenkins: configure credentialsId `docker-creds` for docker registry auth.

## Notes
- Use strong secrets for production and consider external secret manager.
- Replace emptyDir storage with real PV for production.




