# Product-Review
## Deployment Instructions

# React Frontend Deployment Guide (Docker + AWS Elastic Beanstalk)

This guide explains how to deploy the React frontend to AWS Elastic Beanstalk using Docker.

## Prerequisites

- AWS CLI installed and configured (`aws configure`)
- Elastic Beanstalk CLI installed (`pip install awsebcli`)
- Docker installed
- Node.js & npm installed

## 1. Build the Docker Image Locally

```bash
docker build -t react-ebn .
docker run --rm -p 8080:80 react-ebn


---

## 📙 2. `backend/README.md` — Express.js API Deployment on AWS EC2 with Docker

```md
# Backend API Deployment Guide (Express.js + Docker + AWS EC2)

This guide walks through deploying the Node.js (Express) backend to an AWS EC2 instance using Docker.

## 🛠 Prerequisites

- AWS EC2 instance (Ubuntu recommended)
- SSH access to EC2
- Docker & Docker Compose installed on EC2
- Security group with port 80 (or 5000) open

## 📁 Project Structure

backend/
├── Dockerfile
├── .env
├── server.js


## 📦 Dockerfile

```Dockerfile
FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 5000
CMD ["npm", "start"]


