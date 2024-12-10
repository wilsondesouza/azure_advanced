# 🚀 Pipeline de Deploy com Docker e Kubernetes

## 📋 Visão Geral
Este projeto demonstra a implementação de um pipeline de deploy para uma aplicação Node.js utilizando Docker e Kubernetes no Google Cloud Platform (GCP). O projeto está estruturado em duas branches principais, oferecendo diferentes cenários de deployment.

## 🗂️ Estrutura do Projeto

### 📁 /app
Diretório contendo a aplicação Node.js
- **Tecnologias**: JavaScript e HTML
- **Funcionalidade**: Aplicação web base para demonstração do pipeline

### 🐳 Dockerfile
```dockerfile
# Configuração do container para a aplicação Node.js
FROM node:latest
WORKDIR /app
COPY app/ .
RUN npm install
EXPOSE 3000
CMD ["node", "index.js"]
```
**Objetivo**: Define a configuração do container Docker para a aplicação Node.js

### ⚙️ ci.yml
```yaml
# Pipeline de Integração Contínua
stages:
  - build
  - deploy

# Configurações de build e deploy
```
**Finalidade**: Arquivo de configuração do pipeline CI/CD

## 🌟 Cenários de Deploy

### 1️⃣ Cenário Docker
- Deploy da aplicação em container
- Execução isolada e portável
- Facilidade de desenvolvimento e testes

### 2️⃣ Cenário Kubernetes (GCP)
- Deploy em cluster Kubernetes
- Escalabilidade automática
- Gerenciamento robusto de containers

## 🛠️ Pré-requisitos
- Docker Desktop
- Conta GCP
- kubectl CLI
- Node.js
- Git

## 🚀 Como Executar

### Docker Deploy
```bash
# Build da imagem
docker build -t node-app .

# Executar container
docker run -p 3000:3000 node-app
```

### Kubernetes Deploy
```bash
# Configurar GCP
gcloud init

# Deploy no cluster
kubectl apply -f k8s/
```

## 📈 Pipeline CI/CD
1. **Build**: Construção da imagem Docker
2. **Testes**: Verificação da aplicação
3. **Deploy**: Push para registro e deploy no ambiente alvo

## 🎯 Benefícios
- ♻️ Processo automatizado de deploy
- 🛡️ Ambiente isolado e seguro
- 📊 Escalabilidade sob demanda
- 🔄 Facilidade de rollback

## 📚 Documentação Adicional
- [Docker Documentation](https://docs.docker.com/)
- [Kubernetes Documentation](https://kubernetes.io/docs/)
- [GCP Documentation](https://cloud.google.com/docs)