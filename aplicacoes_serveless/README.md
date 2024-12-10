# 🚀 Aplicações Serverless na Azure

## 📋 Visão Geral
Este projeto demonstra a implementação de diferentes serviços serverless na Azure, incluindo Azure Functions, Logic Apps e integrações com outros serviços Azure. O projeto é desenvolvido em C# (100%) e apresenta diversos casos de uso práticos.

## 🗂️ Estrutura do Projeto

### 📁 fn-input-blob
- 📝 Função Azure para processamento de blobs
- 🔗 Integração com Azure Blob Storage
- 📊 Manipulação de arquivos na nuvem

### 📁 fn-ler-sb
- 🔄 Função para leitura do Service Bus
- 📨 Processamento de mensagens assíncronas
- 🔌 Integração com filas e tópicos

### 📁 fn-save-sql
- 💾 Função para salvamento em banco de dados
- 🗄️ Integração com MySQL na Azure
- 📝 Modelo ToDo com campos:
  - id
  - order
  - title
  - url
  - completed

### 📁 fn-simples
- 🎯 Função básica de demonstração
- ⚡ HTTP Trigger simples
- 🔍 Exemplo introdutório

### 📁 fn-tempo
- ⏰ Função baseada em tempo
- 📅 Agendamento de tarefas
- 🔄 Execução periódica

## 🛠️ Configurações Principais

### ⚙️ Logic App
```json
{
    "nome": "",
    "idade": 0
}
```
- 📥 HTTP Trigger com método POST
- 🔗 Integração com Service Bus
- 📤 Resposta HTTP personalizada

### 🔌 Service Bus
1. **Configuração**:
   - Criação do namespace
   - Configuração de políticas de acesso
   - Gerenciamento de filas/tópicos

2. **Conexão**:
   - Shared Access Policies
   - Connection Strings
   - Gerenciamento de permissões

### 🗄️ Banco de Dados
```sql
CREATE TABLE ToDo (
    id INT,
    order INT,
    title VARCHAR(255),
    url VARCHAR(255),
    completed BOOLEAN
);
```

## 🚀 Deploy e Configuração

### 1️⃣ Function App
```bash
# Configuração de ambiente
SqlConnectionString="sua_connection_string"
```

### 2️⃣ Logic App
1. Criar novo Logic App
2. Configurar HTTP Trigger
3. Integrar com Service Bus
4. Definir respostas

## 📊 Arquitetura da Solução
- 🔷 Azure Functions (Processamento)
- 🔷 Logic Apps (Orquestração)
- 🔷 Service Bus (Mensageria)
- 🔷 MySQL (Persistência)

## 🎯 Casos de Uso
1. **Processamento de Arquivos**
   - Upload para Blob Storage
   - Processamento assíncrono
   - Notificações

2. **Integração de Sistemas**
   - Mensageria com Service Bus
   - Persistência em banco de dados
   - Workflows automatizados

## 💡 Dicas de Desenvolvimento
- ✅ Use Consumption Plan para desenvolvimento
- ✅ Configure variáveis de ambiente
- ✅ Implemente logging adequado
- ✅ Utilize managed identity quando possível

## 📚 Recursos Adicionais
- [Azure Functions Documentation](https://docs.microsoft.com/azure/azure-functions/)
- [Logic Apps Documentation](https://docs.microsoft.com/azure/logic-apps/)
- [Service Bus Documentation](https://docs.microsoft.com/azure/service-bus-messaging/)
