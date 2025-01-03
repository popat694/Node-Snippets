This repository serves as a boilerplate for Node.js projects, designed to provide a scalable and maintainable project structure with modern best practices.

---

## Features

- **Modular Architecture**: Clear separation of concerns with organized folders for configuration, controllers, models, routes, services, and more.
- **Sequelize ORM**: Database modeling and migrations for SQL databases.
- **Versioned API Routes**: Easy-to-extend versioning for API endpoints.
- **Custom Middleware**: Authentication, validation, and error-handling middleware.
- **Logging**: Integrated logging system for error and combined logs.
- **Environment Configuration**: Centralized environment variables using `.env`.
- **Testing**: Setup for unit and integration tests using Jest.
- **PM2 Support**: Ecosystem configuration for running and managing the application.
- **Code Quality**: ESLint and Prettier configurations for maintaining clean and consistent code.

---

## Project Structure

```
project-root/
├── src/                    # Source directory
│   ├── config/            # Configuration files
│   │   ├── database.js    # Database configuration
│   │   ├── middleware.js  # Express middleware configuration
│   │   └── config.js      # General configuration (env variables, etc.)
│   │
│   ├── controllers/       # Controller layer - Business logic
│   │   ├── authController.js
│   │   ├── userController.js
│   │   └── index.js       # Controller barrel file
│   │
│   ├── models/           # Data models (Sequelize)
│   │   ├── index.js      # Sequelize model loader
│   │   ├── user.js
│   │   └── role.js
│   │
│   ├── repositories/       # Data access layer
│   │   ├── userRepository.js
│   │   └── index.js        # Repositories barrel file
│   │
│   ├── routes/
│   │   ├── api/
│   │   │   ├── v1/          # Version-specific folder
│   │   │   │   ├── auth.js  # Routes for authentication
│   │   │   │   ├── users.js # Routes for users
│   │   │   │   └── index.js # Index file for v1 routes
│   │   │   └── index.js     # Main API route loader
│   │   └── index.js         # Main route
│   │
│   ├── services/         # Business logic layer
│   │   ├── authService.js
│   │   ├── userService.js
│   │   └── index.js      # Services barrel file
│   │
│   ├── middlewares/      # Custom middleware functions
│   │   ├── auth.js       # Authentication middleware
│   │   ├── validation.js # Request validation middleware
│   │   └── error.js      # Error handling middleware
│   │
│   ├── utils/            # Utility functions and helpers
│   │   ├── logger.js
│   │   ├── validators.js
│   │   └── helpers.js
│   │
│   ├── migrations/       # Database migrations
│   │   └── timestamp-create-users.js
│   │
│   ├── seeders/         # Database seeders
│   │   └── initial-data.js
│   │
│   └── app.js           # Express app initialization
│
├── tests/               # Test files
│   ├── unit/           # Unit tests
│   ├── integration/    # Integration tests
│   └── fixtures/       # Test fixtures
│
├── logs/               # Application logs
│   ├── error.log
│   └── combined.log
│
├── ecosystem.config.js       # PM2 ecosystem configuration
├── .env               # Environment variables
├── .env.example       # Example environment variables
├── .gitignore        # Git ignore file
├── .eslintrc.js      # ESLint configuration
├── .prettierrc       # Prettier configuration
├── jest.config.js    # Jest configuration
├── package.json      # Project dependencies and scripts
└── README.md         # Project documentation
```

## Getting Started

### Prerequisites

- Node.js (v14 or later)
- npm or yarn
- SQL database (e.g., PostgreSQL, MySQL, SQLite)

### Installation

1.Clone the repository:
   ```bash
   git clone <repository-url>
   cd project-root
   ```
2.Install dependencies:
  ```bash
  npm install
  ```
3.Configure environment variables:
  ```bash
  cp .env.example .env
  ```
4.Run database migrations:
  ```bash
  npx sequelize-cli db:migrate
  ```
5.(Optional) Seed the database:
  ```bash
  npx sequelize-cli db:seed:all
  ```
6.Start the application:
---
## Scripts
  - **Start the server**:
   ```bash
   npm start
   ```
  - **Run in development mode:**
    ```bash
    npm run dev
    ```
  - **Run tests:**
    ```bash
    npm test
    ```
  - **Lint the code:**
    ```bash
    npm run lint
    ```
  - **Fix linting issues:**
    ```bash
    npm run lint:fix
    ```

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests to improve this boilerplate.
