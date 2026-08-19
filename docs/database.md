# Database Documentation for FoschiDesk CRM

## Overview
This document outlines the database schema, including tables, relationships and migration scripts.

## Database Schema

### Entities
1. **Client**  
   - `id`: Primary Key  
   - `name`: Client name  
   - `email`: Client email  
   - `phone`: Client phone  

2. **Contact**  
   - `id`: Primary Key  
   - `clientId`: Foreign Key  
   - `name`: Contact name  
   - `email`: Contact email  

3. **Opportunity**  
   - `id`: Primary Key  
   - `clientId`: Foreign Key  
   - `name`: Opportunity name  
   - `status`: Opportunity status  

### Relationships
- **Client** has many **Contacts**  
- **Client** has many **Opportunities**  

## Migration Scripts
1. **Create Client Table**  
   ```sql
   CREATE TABLE Client (
       id SERIAL PRIMARY KEY,
       name VARCHAR(255),
       email VARCHAR(255),
       phone VARCHAR(50)
   );
   ```

2. **Create Contact Table**  
   ```sql
   CREATE TABLE Contact (
       id SERIAL PRIMARY KEY,
       clientId INTEGER REFERENCES Client(id),
       name VARCHAR(255),
       email VARCHAR(255)
   );
   ```

Additional migration scripts follow the same structure.