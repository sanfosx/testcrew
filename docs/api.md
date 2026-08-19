# FoschiDesk API Documentation

## Overview
This document provides a comprehensive overview of the FoschiDesk API, including endpoints, request and response specifications, and authentication requirements.

## API Specification
### Base URL
The base URL for all endpoints is `http://localhost:3000/api`

### Authentication
- JWT is used for authentication. Obtain a token by logging in.
- Include the token in the header for all requests to protected endpoints.

### Endpoints

#### Users
- **POST /auth/login**: Authenticate a user  
  *Request Body*:  
  ```json
  { "username": "string", "password": "string" }
  ```
  *Response*:  
  ```json
  { "token": "string" }
  ```
  
- **GET /users**: Get all users  
  *Response*:  
  ```json
  [{ "id": "integer", "username": "string" }]
  ```

#### Clients
- **POST /clients**: Create a new client  
  *Request Body*:  
  ```json
  { "name": "string", "email": "string", "phone": "string" }
  ```
  *Response*:  
  ```json
  { "clientId": "integer" }
  ```
- **GET /clients**: Get all clients  
  *Response*:  
  ```json
  [{ "id": "integer", "name": "string" }]
  ```

...