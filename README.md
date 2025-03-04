
# Fullstack Next.js, Node.js & PostgreSQL Project

This is a full-stack application template built with Next.js for the frontend, Node.js for the backend, and PostgreSQL as the database. It also includes Docker support for containerization.

## Features

- **Next.js**: Handles the frontend with server-side rendering (SSR) and static site generation (SSG).
- **Node.js**: Manages the backend APIs and services.
- **PostgreSQL**: Used as the relational database for data storage.
- **Docker**: Provides containerization for a consistent development and deployment environment.
- **TypeScript**: Used throughout the project for type safety.

## Prerequisites

Ensure you have the following installed on your system:

- [Node.js](https://nodejs.org/) >= 14
- [Docker](https://www.docker.com/)
- PostgreSQL database

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Subh-Kami/Full-Stack-Web-App.git
   cd fullstack-next-node-postgres
   ```

2. Set up environment variables by creating a `.env` file at the root of the project with the following configuration:

   ```bash
   DATABASE_URL=postgres://username:password@localhost:5432/dbname
   ```

3. Install dependencies:

   ```bash
   cd backend
   npm install
   cd ../frontend
   npm install
   ```

4. Start the PostgreSQL database using Docker:

   ```bash
   docker-compose up
   ```

5. Run the backend and frontend servers:

   ```bash
   cd backend
   npm run dev
   cd ../frontend
   npm run dev
   ```

6. Access the application at `http://localhost:3000`.

## Folder Structure

- **backend/**: Contains the Node.js API, with routes and services interacting with the PostgreSQL database.
- **frontend/**: Next.js frontend application with pages, components, and SSR configuration.
- **docker-compose.yaml**: Docker configuration for PostgreSQL.

## Development

- For frontend development, modify files inside the `frontend/` directory.
- For backend API changes, update files inside the `backend/` directory.

## Contributing

Feel free to contribute by opening issues or submitting pull requests.

---

Happy coding!
