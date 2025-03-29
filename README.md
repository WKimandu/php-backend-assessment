# PHP Backend Assessment

Welcome to the PHP Backend Technical Assessment! This repository contains a project designed to evaluate your skills in PHP backend development.

## Overview

In this assessment, you'll build a RESTful API using Laravel/Lumen that serves as the backend for a content management system with:
- User authentication and authorization
- Data model design and implementation
- RESTful API endpoints
- Database interactions
- Testing

## Assessment Goals

This assessment evaluates your ability to:
1. Create a well-structured Laravel/Lumen application
2. Design and implement database models and relationships
3. Build RESTful API endpoints with proper validation
4. Implement authentication and authorization
5. Write tests for your API endpoints
6. Follow best practices for PHP development

## Project Description

### Content Management API

You'll develop a backend API for a content management system with the following features:

1. **User Management**
   - Registration and login
   - Role-based authorization (Admin, Editor, Viewer)
   - Password reset functionality

2. **Content Management**
   - Create, read, update, and delete articles
   - Categories and tags for articles
   - Media uploads (images)
   - Content status (draft, published, archived)

3. **Comments**
   - Add comments to articles
   - Moderation capabilities
   - Nested replies

## Getting Started

### Prerequisites
- PHP 8.0+
- Composer
- MySQL/PostgreSQL
- Git

### Setup Instructions

1. Clone this repository
2. Create a branch with your name: `git checkout -b candidate/your-name`
3. Install dependencies:
   ```
   composer install
   ```
4. Set up environment:
   - Copy `.env.example` to `.env`
   - Configure your database connection
   - Generate application key: `php artisan key:generate`

5. Run migrations and seeders:
   ```
   php artisan migrate --seed
   ```

6. Start the development server:
   ```
   php artisan serve
   ```

## Development Guidelines

- Follow the instructions in TODOs throughout the codebase
- Use Laravel conventions and best practices
- Implement proper validation for all inputs
- Document your API endpoints (can use Laravel API Documentation tools)
- Write both unit and feature tests
- Commit frequently with meaningful commit messages
- Do not modify the CI/CD configuration

## Evaluation Criteria

Your submission will be evaluated on:

| Category      | Weight | Description                                                |
| ------------- | ------ | ---------------------------------------------------------- |
| Functionality | 30%    | Completion of required features and correct business logic |
| Code Quality  | 30%    | Clean, maintainable code that follows best practices       |
| API Design    | 20%    | RESTful design, proper status codes, validation            |
| Testing       | 20%    | Comprehensive test coverage and quality                    |

## Submission

When you've completed the assessment:

1. Ensure all tests pass: `php artisan test`
2. Commit and push your changes
3. Create a pull request to the main branch
4. Include a brief description of your approach, challenges faced, and any improvements you'd make with more time

## API Documentation

Once complete, your API should support the following endpoints (at minimum):

### Authentication
- `POST /api/register` - Register a new user
- `POST /api/login` - Login and get access token
- `POST /api/logout` - Logout and invalidate token

### Articles
- `GET /api/articles` - List all articles (with pagination)
- `GET /api/articles/{id}` - Get a specific article
- `POST /api/articles` - Create a new article
- `PUT /api/articles/{id}` - Update an article
- `DELETE /api/articles/{id}` - Delete an article

### Categories
- `GET /api/categories` - List all categories
- `POST /api/categories` - Create a new category (admin only)

### Comments
- `GET /api/articles/{id}/comments` - Get comments for an article
- `POST /api/articles/{id}/comments` - Add a comment to an article

## Support

If you have any questions or encounter issues, please create an issue in this repository or contact the assessment coordinator.

Good luck! 