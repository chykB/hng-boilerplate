# FastAPI Project Documentation

## Table of Contents
1. [Introduction](#introduction)
2. [API Design](#api-design)
   - [Endpoints Overview](#endpoints-overview)
3. [Database Design](#database-design)
   - [Entity-Relationship Diagram](#entity-relationship-diagram)
   - [Table Schemas](#table-schemas)


## Introduction
This task requires us to work in a team to contribute to an open-source project by designing API and database. Here’s a step-by-step breakdown of what we did:

## API Design
We created a complete and detailed API design documented using OpenAPI. Here is the [Link](https://app.swaggerhub.com/apis-docs/ISRAELBOLUWATIFE17/hng-task/0.1.0#/Auth/signup)

### Endpoints Overview
Here is the list of all the API endpoints:


#### Create User
- **URL**: `/signup`
- **Method**: POST
- **Description**: This endpoint create a user.
- **Returns**: Created User.

#### Login User
- **URL**: `/login`
- **Method**: POST
- **Description**: Endpoint login a user.
- **Returns**: Logged in User and access token.

#### Get User
- **URL**: `/user`
- **Method**: GET
- **Description**: Endpoint gets a user information.
- **Returns**: Returns an authenticated user information

#### Get User
- **URL**: `/refresh-access-token`
- **Method**: GET
- **Description**: Endpoint refresh access token.
- **Returns**: Refreshes an access_token with the issued refresh_token Parameters ---------- refresh_token : str, None The refresh token sent in the cookie by the client (default is None)

#### Logout User
- **URL**: `/logout`
- **Method**: POST
- **Description**: This endpoint logs out an authenticated user.
- **Returns message**: User logged out successfully.

#### Delete User
- **URL**: `/users/{user_id}`
- **Method**: DELETE
- **Description**: This endpoint deletes a user from the db. (Soft delete)
- **Returns message**: User deleted successfully.

#### Create User Roles
- **URL**: `/users/roles`
- **Method**: POST
- **Description**: Endpoint to create custom roles for users mixing permissions.
- **Returns**: Created user.




## Database Design

### Entity-Relationship Diagram
![Image](./dbdesign-image/dbdesign.png)

### Table Schemas
- Table Name: users
- Description: This table contains a user credentials

#### Users Table
| Column Name | Type | Constraints |
|-------------|------|-------------|
| id | bigint | PRIMARY KEY |
| unique_id | VARCHAR(255) | NOT NULL |
| first_name | VARCHAR(255) | 
| last_name | VARCHAR(255) | 
| email | VARCHAR(500) | NOT NULL |
| password | VARCHAR(500) | NOT NULL |
| is_active | bool | 
| date_created | datetime | 
| last_updated | datetime | 
| is_active | bool |


- Table Name: blacklist_tokens
- Description: Blacklist tokens

#### Users Table
| Column Name | Type | Constraints |
|-------------|------|-------------|
| id | int | PRIMARY KEY |
| created_by | bigint | FOREIGN_KEY |
| token | VARCHAR(255) | 
| date_created | datetime | 



## Contributors to this project:
[Our Slack usernames]

