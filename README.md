# ✈️ TravelFlow

## Travel Planning & Management System

TravelFlow is a full-stack web application that simplifies travel planning through one centralized platform. Users can create and manage trips, prepare day-wise itineraries, track expenses and budgets, discover tourist attractions, and navigate using Google Maps.

## 🚀 Features

- **Authentication & Security:** User registration, login, JWT authentication, and protected routes.
- **Trip Management:** Create, view, update, and delete trips.
- **Itinerary Management:** Organize daily activities and manage itinerary dates.
- **Expense Management:** Add, update, categorize, and delete travel expenses.
- **Budget Tracking:** Calculate total expenses, remaining budget, and budget summaries.
- **Tourist Attraction Discovery:** Find attractions using Geoapify.
- **Google Maps Navigation:** Open attractions and directions in Google Maps.
- **Dashboard:** View trip counts, budgets, expenses, and remaining balances.

## 🛠️ Technology Stack

**Frontend**
- React
- Vite
- JavaScript
- HTML5 and CSS3

**Backend**
- Java 21
- Spring Boot
- Spring Security
- JWT Authentication
- Spring Data JPA
- REST APIs
- Maven

**Database and External Services**
- MySQL
- Geoapify Places API
- Google Maps

**Tools**
- Visual Studio Code, Postman, Git, GitHub, npm

## 🏗️ System Architecture

```text
React Frontend
      |
      v
Spring Security + JWT
      |
      v
REST Controllers
      |
      v
Service Layer
      |
      v
Repository Layer
      |
      v
MySQL Database
```

The backend also communicates with Geoapify to retrieve tourist attractions.

## 🔄 Backend Workflow

1. The React frontend sends an HTTP request to the Spring Boot backend.
2. Spring Security checks authentication for protected endpoints.
3. The JWT filter validates the user's token.
4. The REST Controller receives the request.
5. The Service Layer processes business logic.
6. Spring Data JPA communicates with MySQL through repositories.
7. The backend returns a response to the frontend.
8. The backend uses Geoapify for attraction discovery.

## 🔌 REST API Endpoints

**Authentication**
- `POST /api/auth/register`
- `POST /api/auth/login`

**Trips**
- `POST /api/trips`
- `GET /api/trips`
- `PUT /api/trips/{id}`
- `DELETE /api/trips/{id}`

**Itineraries**
- `GET /api/trips/{tripId}/itineraries`
- `POST /api/trips/{tripId}/itineraries`
- `PUT /api/trips/{tripId}/itineraries/{itineraryId}`
- `DELETE /api/trips/{tripId}/itineraries/{itineraryId}`

**Expenses**
- `GET /api/trips/{tripId}/expenses`
- `POST /api/trips/{tripId}/expenses`
- `PUT /api/trips/{tripId}/expenses/{expenseId}`
- `DELETE /api/trips/{tripId}/expenses/{expenseId}`

**Other**
- `GET /api/dashboard`
- `GET /api/trips/{tripId}/budget-summary`
- `GET /api/places/destination-attractions?destination={destination}`

## ⚙️ Installation and Setup

### Prerequisites

- Java 21 or later
- Maven
- MySQL
- Node.js and npm
- Git

### Clone the Repository

Clone the backend and frontend repositories separately:

```bash
git clone https://github.com/kalletivansh/TravelFlow-Backend.git
git clone https://github.com/kalletivansh/TravelFlow-Frontend.git
```

### Configure Environment Variables

Configure the required database credentials and Geoapify API key in your environment. The deployed backend also requires `DB_URL` and any other application-specific secrets configured in Render.

Required variables include:

```text
DB_URL
DB_USERNAME
DB_PASSWORD
GEOAPIFY_API_KEY
```

Never commit passwords, API keys, or JWT secrets to a public repository.

### Run the Backend Locally

From the backend project directory:

```bash
mvn spring-boot:run
```

Local backend: `http://localhost:8080`

### Run the Frontend Locally

From the frontend project directory:

```bash
npm install
npm run dev
```

Local frontend: `http://localhost:5173`

## 🌐 Live Deployment

- **Frontend:** https://travel-flow-frontend.vercel.app/
- **Backend:** https://travelflow-backend-e6yi.onrender.com

## 🔒 Security

- JWT-based authentication
- Spring Security for protected APIs
- Environment variables for database credentials and API keys
- Protected frontend routes

## 🔮 Future Enhancements

- AI-based itinerary recommendations
- Hotel and flight integrations
- Weather information
- Collaborative trip planning
- Trip sharing and notifications
- Advanced expense analytics
- Mobile application

## 👨‍💻 Developer

**Kalleti Vamshi**  
B.Tech – Computer Science and Engineering  
Anurag University  
2024–2028

## 📚 Project Purpose

TravelFlow demonstrates full-stack Java development, React frontend development, REST API design, MySQL integration, JWT authentication, external API integration, trip management, itinerary planning, and expense tracking.

**Plan. Organize. Explore.**