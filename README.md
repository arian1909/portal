# Portal Application

## Overview
Portal aplikasi Vue.js yang di-deploy menggunakan Azure App Service dengan Docker container.

## Deployment Information
- **App Service Name**: portal-webapp-arian
- **Resource Group**: rg-arianbarker1909
- **URL**: https://portal-webapp-arian.azurewebsites.net
- **Docker Image**: arian1909/portal:latest

## Architecture
- **Frontend**: Vue.js dengan Vuetify
- **Web Server**: Nginx
- **Container Registry**: Docker Hub
- **Cloud Platform**: Azure App Service
- **CI/CD**: GitHub Actions

## Setup Instructions

### Prerequisites
- Node.js 16+
- Docker
- Azure CLI
- Git

### Local Development
```bash
npm install
npm run serve
```

### Docker Build
```bash
docker build -t arian1909/portal:latest .
docker push arian1909/portal:latest
```

### Azure Deployment
1. Login to Azure
2. Create App Service Plan
3. Create Web App with container
4. Configure container settings

### CI/CD Pipeline
GitHub Actions workflow ter-trigger otomatis pada:
- Push ke branch main
- Pull request ke main
- Manual trigger

## Required Secrets
Untuk GitHub Actions, tambahkan secrets berikut:
- `DOCKER_USERNAME`: Username Docker Hub
- `DOCKER_PASSWORD`: Password Docker Hub
- `AZURE_CREDENTIALS`: JSON credentials untuk Azure

## Contributors
- luke.edwards@flexidev.co
- dion.sasmito@flexidev.co
- cininta.golda@flexidev.co