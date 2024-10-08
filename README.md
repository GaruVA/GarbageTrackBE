# GarbageTrack Backend

This repository hosts the backend server for the **GarbageTrack** application, a waste collection tracking and request system for urban areas.

## Prerequisites

Ensure you have the following installed on your machine before setting up the project:

- **Node.js** (v14 or later)
- **npm** (Node Package Manager)
- A **MongoDB Atlas** account for database management

## Getting Started

Follow these steps to set up the project locally:

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd garbagetrack-backend
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Environment configuration**:
   - Create a `.env` file in the root directory and add the following environment variables:
     ```env
     MONGODB_URI=<your-mongodb-uri>
     PORT=5000
     ```
   - Replace `<your-mongodb-uri>` with your actual MongoDB connection string from MongoDB Atlas.

4. **Start the development server**:
   ```bash
   npm run dev
   ```

   The backend server should now be running at `http://localhost:5000`.

## Available Scripts

- **`npm run dev`**: Starts the development server with hot-reloading using `ts-node-dev`.
- **`npm run build`**: Compiles the TypeScript code into JavaScript, generating the `dist` folder.
- **`npm start`**: Runs the production server using the compiled JavaScript files.

## Project Structure

The project follows a modular structure for easier maintenance and scalability:

```
garbagetrack-backend/
│
├── src/                    # TypeScript source code
│   ├── config/             # Configuration files (e.g., database connection)
│   ├── models/             # Mongoose models defining data schemas
│   ├── routes/             # Express route handlers
│   ├── controllers/        # Route controllers with business logic
│   └── middlewares/        # Custom middleware functions
│
├── dist/                   # Compiled JavaScript code (after running build)
│
├── .env                    # Environment variables (do not commit this file)
├── package.json            # Project metadata and dependencies
└── tsconfig.json           # TypeScript configuration file
```
