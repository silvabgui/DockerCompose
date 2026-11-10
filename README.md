 # 🐳 Ambiente Docker Compose: Nginx & Whoami

Um projeto prático de orquestração de containers desenvolvido para consolidar conhecimentos em infraestrutura e Docker. Este ambiente sobe simultaneamente um site estático customizado e uma aplicação HTTP leve para testes de rede.

## 📦 Estrutura dos Serviços

O ambiente é gerido pelo `docker-compose.yml` e orquestra dois containers:

1. **site-estatico (Nginx):** 
   - Utiliza uma imagem customizada construída a partir do `nginx:alpine`.
   - Serve uma página HTML estática (`index.html`).
   - Mapeado para a porta **8080**.

2. **app-simples (Whoami):**
   - Utiliza a imagem pública `traefik/whoami`.
   - Um servidor web minimalista que devolve informações do sistema operativo e detalhes do pedido HTTP recebido.
   - Mapeado para a porta **8081**.

## 🚀 Pré-requisitos

Para correr este projeto na sua máquina, precisa de ter instalado:
* [Docker Desktop](https://www.docker.com/products/docker-desktop/) (com a engine a correr em background).
* Git (para clonar o repositório).

## 🚀 Passo a Passo de Execução

1. Buildar a imagem customizada:
No terminal, na pasta do projeto, execute:
   ```bash
   docker build -t meu-site-nginx .
   

2. Testar nos navegadores:

* Site estático: http://localhost:8080.
* App Whoami: http://localhost:8081.

3. Explorar comandos extras:

* Ver containers ativos: 
   ```bash
    docker compose ps
* Ver logs em tempo real:
   ```bash
   docker compose logs -f
* Acessar o terminal do Nginx:
   ```bash
   docker compose exec site-estatico sh

5. Finalizar o ambiente:
Para parar e remover os containers, redes e volumes:
   ```bash
   docker compose down

## 👨‍💻 Autores
Guilherme da Silva Bispo
Adilson de Sousa Santos

Sistemas de Informação
