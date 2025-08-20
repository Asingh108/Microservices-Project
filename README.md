# Microservices-Project
# Auth & File Upload Microservice(Node.js+Express)

This project contains two simple backend microservices:
1. *Auth Service*  
   - User registration & login with JWT  
   - Passwords hashed using bcrypt  
   - MongoDB for user storage  
2. *File Service*  
   - Upload files (max 50MB, raw binary – not multipart)  
   - Files saved to AWS S3  
   - Metadata (filename, size, userId, S3 key) stored in MongoDB  
   - Protected with JWT authentication

## Setup
### Requirements
- Node.js >= 16  
- MongoDB running locally or on Atlas  
- AWS S3 bucket + credentials

## Auth Service and File Service
### Start
### Install
```bash
cd auth/file
npm install
npm start

## Architecture
    [Client]
       |
    JWT Login
       |
  [Auth Service] --- MongoDB(Users)
       |
   Issues JWT
       |
    [Client]
