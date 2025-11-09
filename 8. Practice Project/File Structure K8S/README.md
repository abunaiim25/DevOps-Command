# DEPLOYMENT Repo Template
# Kubernetes Deployment Templates

এই repo-তে রয়েছে আমাদের Project এর সব Kubernetes Deployment, Service, Ingress, CronJob, RBAC এবং Redis এর YAML ফাইলগুলো।  
এছাড়াও Jenkinsfile গুলো দিয়ে CI/CD Pipeline তৈরি করা হয়েছে।  

## Folder Structure

- `bida-moha-api/` : bida-moha-api service এর Deployment, Service, Ingress
- `bidaapi/` : bidaapi service এর Deployment, Service, Ingress
- `custom-resource/` : HPA, PDB, PriorityClass
- `jobs/` : CronJob এবং DB backup jobs
- `network/` : NetworkPolicy, Service, Ingress
- `RBAC/` : Role, RoleBinding, ServiceAccount
- `redis/` : Redis Deployment, Service, Config
- `deploy.yaml` : সব services একসাথে deploy করার template
- `Jenkinsfile*` : CI/CD pipeline template

## Usage

1. Docker image build & push
2. `kubectl apply -f <folder-or-file>` দিয়ে deploy
3. Jenkinsfile অনুযায়ী CI/CD চালানো যায়


DEPLOYMENT/
│
├── bida-moha-api/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── ingress.yaml
│
├── bidaapi/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── ingress.yaml
│
├── custom-resource/
│   ├── hpa.yaml
│   ├── pdb.yaml
│   └── priorityclass.yaml
│
├── jobs/
│   ├── cronjob-cleanup.yaml
│   └── db-backup.yaml
│
├── network/
│   ├── ingress.yaml
│   ├── networkpolicy.yaml
│   └── service.yaml
│
├── RBAC/
│   ├── role.yaml
│   ├── rolebinding.yaml
│   └── serviceaccount.yaml
│
├── redis/
│   ├── redis-deploy.yaml
│   ├── redis-service.yaml
│   └── redis-config.yaml
│
├── deploy.yaml
│
├── Jenkinsfile
├── JenkinsfileAPI
├── JenkinsfileCron
├── JenkinsfileMoha
│
└── README.md


----------------------------------

DEPLOYMENT/
│
├── frontend/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── ingress.yaml
│
├── backend-api/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── ingress.yaml
│
├── database/
│   ├── mysql-deploy.yaml
│   ├── mysql-service.yaml
│   └── mysql-config.yaml
│
├── redis/
│   ├── redis-deploy.yaml
│   ├── redis-service.yaml
│   └── redis-config.yaml
│
├── custom-resource/
│   ├── hpa.yaml
│   ├── pdb.yaml
│   └── priorityclass.yaml
│
├── jobs/
│   ├── cronjob-cleanup.yaml
│   └── db-backup.yaml
│
├── network/
│   ├── ingress.yaml
│   ├── networkpolicy.yaml
│   └── service.yaml
│
├── RBAC/
│   ├── role.yaml
│   ├── rolebinding.yaml
│   └── serviceaccount.yaml
│
├── deploy.yaml
│
├── Jenkinsfile
├── JenkinsfileFrontend
├── JenkinsfileAPI
├── JenkinsfileCron
│
└── README.md
