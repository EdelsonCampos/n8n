# 🤖 Stack de Automação: n8n + Multi-WAHA

Este repositório contém a infraestrutura completa para um ambiente de automação profissional utilizando Docker. O diferencial deste projeto é a capacidade de gerenciar múltiplos números de WhatsApp simultaneamente, contornando as limitações da versão gratuita do WAHA.

## 🚀 Tecnologias Utilizadas

* **n8n**: Plataforma de automação de fluxo de trabalho baseada em nós.
* **WAHA (WhatsApp HTTP API)**: Duas instâncias independentes para conexão de múltiplos aparelhos.
* **PostgreSQL**: Banco de dados robusto para persistência das automações.
* **Redis**: Gerenciamento de cache e filas para alta performance.

## 🏗️ Arquitetura Multi-Instância

Para permitir o uso de mais de um número no plano **WAHA Core**, a stack foi configurada com contêineres isolados:
* **Instância 1**: Disponível em `http://localhost:3000`.
* **Instância 2**: Disponível em `http://localhost:3001`.

## 📦 Como Instalar

1.  Certifique-se de ter o **Docker** e **Docker Compose** instalados.
2.  Clone este repositório:
    ```bash
    git clone [https://github.com/EdelsonCampos/n8n.git](https://github.com/EdelsonCampos/n8n.git)
    ```
3.  Acesse a pasta e suba os serviços:
    ```bash
    docker-compose up -d
    ```

## 🔒 Segurança

O projeto inclui um arquivo `.gitignore` configurado para garantir que dados sensíveis, como sessões de WhatsApp, mídias e bancos de dados locais, nunca sejam enviados para o repositório público.
