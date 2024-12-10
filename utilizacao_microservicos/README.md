# 🐳 Utilização prática no cenário de Microsserviços

## 📁 Overview
Este projeto demonstra uma implementação prática do Docker em uma arquitetura de microsserviços. Inclui arquivos de configuração e código para configurar um aplicativo da web básico com PHP e MySQL.

## 🗂️ Estrutura do Repositório
O repositório contém os seguintes arquivos de chave:

### 📜 dockerfile
```dockerfile
FROM nginx:latest
COPY nginx.conf /etc/nginx/nginx.conf
COPY index.php /usr/share/nginx/html/
RUN apt-get update && apt-get install -y php-fpm
```
Este arquivo configura um servidor web Nginx com suporte a PHP:
- Usa a imagem mais recente do Nginx como base
- Configura o Nginx usando uma configuração personalizada
- Copia o arquivo do aplicativo PHP
- Instala o PHP-FPM para processamento PHP

### 🌐 nginx.conf
O arquivo de configuração do Nginx define:
- Configurações do servidor
- Regras de processamento PHP
- Configurações do servidor HTTP
- Manipulação de arquivos estáticos

### 💻 index.php
O acesso principal em PHP faz:
- Conecta-se ao banco de dados MySQL
- Lida com envios de formulários
- Exibe a interface do usuário

### 🗄️ banco.sql
Arquivo SQL contendo:
- Esquema de banco de dados
- Configuração inicial de dados
- Definições de tabela
- Configurações de banco de dados necessárias

## 🚀 Começando
1. Clone o repositório
2. Crie a imagem do Docker:
```bash
docker build -t my-php-app .
```
3. Execute o contêiner:
```bash
docker run -p 80:80 my-php-app
```

## 🛠️ Pré-requisitos
- Conhecimento em Linux
- Docker
- Conhecimento em Nuvem

## 🎯 Objetivos de aprendizagem
- Noções básicas sobre a conteinerização do Docker
- Implementação da arquitetura de microsserviços
- Gerenciando configurações de Nginx e PHP
- Integração de banco de dados em ambientes conteinerizados
