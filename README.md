# Portal Application

## Overview
Vue.js portal application deployed using Azure App Service with Docker container.

## Deployment Information
- **App Service Name**: portal-webapp-arian
- **Resource Group**: rg-arianbarker1909
- **URL**: https://portal-arian-flexidev.yankers.fun (Custom Domain)
- **Fallback URL**: https://portal-webapp-arian.azurewebsites.net
- **Docker Image**: arian1909/portal:latest

## Architecture
- **Frontend**: Vue.js with Vuetify
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
GitHub Actions workflow automatically triggers on:
- Push to main branch
- Pull request to main
- Manual trigger

## Required Secrets
For GitHub Actions, add the following secrets:
- `DOCKER_USERNAME`: Docker Hub Username
- `DOCKER_PASSWORD`: Docker Hub Password
- `AZURE_CREDENTIALS`: JSON credentials for Azure

## Contributors
- luke.edwards@flexidev.co
- dion.sasmito@flexidev.co
- cininta.golda@flexidev.co

## Test CI/CD
