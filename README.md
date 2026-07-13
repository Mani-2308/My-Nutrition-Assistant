# Nutrition Assistant

Nutrition Assistant is a full-stack web application for tracking meals, calculating nutrition, generating diet plans, and managing user profiles. The project includes a React frontend and an Express/MongoDB backend with Firebase authentication support.

## Features

- User registration and login
- Profile management
- Meal tracking and daily summaries
- Food search using USDA FoodData Central API
- Nutrition calculations and diet plan generation
- BMI and water intake calculations
- Protected API routes with JWT authentication

## Tech Stack

- Frontend: React, React Router, Bootstrap, Firebase Auth, Chart.js
- Backend: Node.js, Express, MongoDB, Mongoose, JWT, bcrypt
- APIs: USDA FoodData Central

## Repository Structure

- `client/` - React frontend application
- `server/` - Express backend API

## Prerequisites

- Node.js (v18+ recommended)
- npm
- MongoDB database or MongoDB Atlas cluster

## Setup

### 1. Install dependencies

Open two terminals or run sequentially:

```powershell
cd c:\Users\kodal\Downloads\My-Nutrition-Assistant\Nutrition-Assistant-main\server
npm install

cd ..\client
npm install
```

### 2. Configure backend environment variables

Create a `.env` file inside `server/` with:

```env
MONGO_URI=<your_mongodb_connection_string>
JWT_SECRET=<your_jwt_secret>
USDA_API_KEY=<your_usda_api_key>
```

If you do not have a USDA API key yet, request one from the USDA FoodData Central website.

### 3. Run the backend

```powershell
cd c:\Users\kodal\Downloads\My-Nutrition-Assistant\Nutrition-Assistant-main\server
npm run dev
```

The backend listens on `http://localhost:8000` by default.

### 4. Run the frontend

```powershell
cd c:\Users\kodal\Downloads\My-Nutrition-Assistant\Nutrition-Assistant-main\client
npm start
```

The React app runs on `http://localhost:3000` by default.

## Notes

- The backend requires `MONGO_URI`, `JWT_SECRET`, and `USDA_API_KEY` to start successfully.
- The frontend uses Firebase configuration in `client/src/firebase.js`. If you want your own Firebase project, replace that config with your own values.
- API routes are prefixed with `/api/users` from the server.

## Available Scripts

### Backend

- `npm start` - Run server in production mode
- `npm run dev` - Run server with nodemon for development

### Frontend

- `npm start` - Start React development server
- `npm run build` - Build React app for production
- `npm test` - Run React tests

## API Endpoints

- `POST /api/users/register` - Register new user
- `POST /api/users/login` - Login user
- `GET /api/users/profile` - Get current user profile (protected)
- `PUT /api/users/profile` - Update current user profile (protected)
- `POST /api/users/food` - Search foods using USDA API
- `POST /api/users/nutrition` - Calculate nutrition summary (protected)
- `GET /api/users/diet` - Get diet plan (protected)
- `POST /api/users/water` - Calculate water intake (protected)
- `POST /api/users/bmi` - Calculate BMI (protected)
- `POST /api/users/meal` - Add meal (protected)
- `GET /api/users/meals` - Get meals (protected)
- `DELETE /api/users/meal/:id` - Delete a meal (protected)
- `GET /api/users/summary` - Get daily summary (protected)
- `GET /api/users/weekly-summary` - Get weekly summary (protected)

## License

This project is provided as-is.
