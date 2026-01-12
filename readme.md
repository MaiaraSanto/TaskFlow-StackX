<div align="center">
🗂️ TaskFlow – Gerenciador de Tarefas
<div align="center"> <img src="frontend/public/doc.png" alt="Documentação" height="35" />

🚀 Acesse e Crie Suas Tarefas


📖 Índice

Sobre o Projeto

Objetivo

Tecnologias Utilizadas

Documentação da API

Instalação e Configuração

Pré-requisitos

FrontEnd

BackEnd

Docker

Execução do Projeto

Banco de Dados

Frontend

Branches e Implementações

Licença

Autor

📌 Sobre o Projeto

TaskFlow é um sistema completo de gerenciamento de tarefas que integra frontend em React, backend em Node.js/Express, e banco de dados PostgreSQL, com toda a aplicação preparada para containerização via Docker. Ideal para organização pessoal ou equipes pequenas.

🎯 Objetivo

O objetivo do projeto é fornecer uma solução robusta e moderna para criação, acompanhamento e gerenciamento de tarefas, permitindo aos usuários registrar, atualizar e organizar suas atividades de forma eficiente.

💻 Tecnologias Utilizadas
Backend








Frontend








DevOps & Ferramentas




📚 Documentação da API

A API possui endpoints principais para gerenciamento de usuários e tarefas:

POST /api/auth/register → Criar usuário

POST /api/auth/login → Autenticar usuário

GET /api/tasks → Listar tarefas

POST /api/tasks → Criar tarefa

PUT /api/tasks/:id → Atualizar tarefa

🔗 Abrir no Postman

🛠️ Instalação e Configuração
Pré-requisitos

Node.js v18+

Docker v20+

PostgreSQL 15

📦 FrontEnd

Criar projeto React via Vite

npm create vite@latest . -- --template react


Instalar dependências

npm install axios react-router-dom react-icons react-toastify @heroicons/react date-fns


Configurar TailwindCSS

npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p

📦 BackEnd

Instalar dependências

npm install express express-async-handler cors dotenv bcryptjs jest jsonwebtoken nodemon sequelize

🐳 Docker

Windows/macOS

Instale o Docker Desktop: Download

Inicie o serviço e verifique se está rodando.

Linux

sudo apt-get update
sudo apt-get install -y apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
sudo apt-get install -y docker-ce docker-ce-cli containerd.io
sudo usermod -aG docker $USER
newgrp docker


Verificar instalação

docker --version
docker run hello-world

Dependências gerais
npm install
npm list

🚀 Execução do Projeto

Rodar todos os serviços com Docker

docker-compose -f docker/docker-compose.yml up --build


Portas padrão:

Backend: 5000

Frontend: 5173

PostgreSQL: 5432

Parar todos os serviços

docker-compose -f docker/docker-compose.yml down -v


Limpar recursos Docker

docker system prune -a
docker volume prune

🗄️ Banco de Dados (PostgreSQL)

Acessar localmente

docker exec -it postgres-db psql -U postgres -d taskmanager


Acessar via Neon

psql "postgresql://[DB_USER]:[DB_PASSWORD]@[DB_HOST]/taskmanager?sslmode=require"


Comandos úteis

\dt  -- listar tabelas
\d "Tasks"  -- descrever tabela Tasks
SELECT * FROM "Tasks";  -- consultar todos os registros

🖥️ Frontend

Desenvolvimento

npm run dev


Build produção

npm run build


Porta frontend dev: 5180

🌿 Branches e Implementações

Frontend

release/desenvolvimento-front-end

Backend

release/desenvolvimento-back-end

📄 Licença

Este projeto está sob MIT License.

