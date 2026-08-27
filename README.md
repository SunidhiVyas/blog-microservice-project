# Blog Microservices Platform

A full-stack blog platform built using a microservices architecture.

The project allows users to sign in with Google, create and manage blogs, generate blog titles and descriptions using AI, and interact with blogs through a modern web interface.

## Features

- Google OAuth authentication
- User registration and authentication
- Create, edit and delete blogs
- AI-powered blog title and description generation
- Image upload using Cloudinary
- Redis caching
- RabbitMQ message communication
- Separate microservices for users, authors and blogs
- Responsive Next.js frontend
- MongoDB/Neon database integration

## Tech Stack

### Frontend
- Next.js
- React
- TypeScript
- Tailwind CSS
- Axios

### Backend
- Node.js
- Express.js
- TypeScript
- MongoDB
- Neon/PostgreSQL

### Other Technologies
- RabbitMQ
- Redis
- Cloudinary
- Google OAuth
- Gemini AI
- Docker

## Microservices

The backend is divided into three services:

### User Service

Handles:

- User authentication
- Google OAuth
- User profiles
- JWT authentication

Runs on:

```text
http://localhost:5000

Running the Project Locally
1. Clone the repository
git clone https://github.com/SunidhiVyas/blog-microservice-project.git
cd blog-microservice-project
2. Install dependencies

Install frontend dependencies:

cd frontend
npm install

Install dependencies for each backend service:

cd ../services/user
npm install
cd ../services/author
npm install
cd ../services/blog
npm install
3. Configure environment variables

Create .env files based on the provided .env.example files:

services/user/.env.example
services/author/.env.example
services/blog/.env.example

Add your own:

MongoDB/Neon credentials
Google OAuth credentials
Cloudinary credentials
Gemini API key
RabbitMQ configuration
Redis configuration
JWT secret

Never commit .env files or API keys to GitHub.

4. Start RabbitMQ

Make sure Docker Desktop is running.

docker start blog-rabbitmq
5. Start Redis
docker start blog-redis

Check both containers:

docker ps
6. Start the services

Start User Service:

cd services/user
npm start

Start Author Service:

cd services/author
npm start

Start Blog Service:

cd services/blog
npm start
7. Start the frontend
cd frontend
npm run dev

Open:

http://localhost:3000
Docker Services

The project uses Docker containers for:

RabbitMQ → localhost:5672
RabbitMQ Management → localhost:15672
Redis → localhost:6379

RabbitMQ Management UI:

http://localhost:15672