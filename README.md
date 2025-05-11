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

