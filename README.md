✈️ TravelFlow
Travel Planning & Management System
TravelFlow is a full-stack web application designed to simplify and organize travel planning through a centralized platform. It allows users to securely create and manage trips, prepare day-wise itineraries, track expenses and budgets, discover tourist attractions, and navigate to places using Google Maps.

🚀 Features
🔐 Authentication & Security
User registration and login
JWT-based authentication
Spring Security integration
Protected frontend routes
Secure access to user-specific travel data
🧳 Trip Management
Create trips
View planned trips
Update trip details
Delete trips
Manage destination, travel dates, budget, and description
📅 Itinerary Management
Create day-wise activities
View itinerary items
Update activities
Delete activities
Validate itinerary dates according to trip dates
💰 Expense & Budget Management
Add travel expenses
Categorize expenses
Update expenses
Delete expenses
Validate expense dates
Calculate total expenses
Calculate remaining budget
Generate budget summaries
🏛️ Tourist Attraction Discovery
Search attractions based on trip destination
Retrieve tourist places using Geoapify
Display attraction names and addresses
Open attractions directly in Google Maps
🗺️ Google Maps Navigation
View tourist attractions on Google Maps
Get directions to selected attractions
Uses Google Maps URLs without requiring a paid Google Maps API
📊 Dashboard
The dashboard provides a summary of:

Total trips
Upcoming trips
Total planned budget
Total expenses
Remaining budget
🛠️ Technology Stack
Frontend
React
Vite
JavaScript
HTML5
CSS3
Backend
Java
Spring Boot
Spring Security
JWT Authentication
Spring Data JPA
REST APIs
Maven
Database
MySQL
External Services
Geoapify Places API
Google Maps
Development Tools
Visual Studio Code
Postman
Git
GitHub
Maven
npm
🏗️ System Architecture
TravelFlow follows a layered architecture:

React Frontend
      |
      | REST API Requests
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
The backend also communicates with Geoapify to retrieve tourist attractions, while Google Maps URLs provide location viewing and navigation.

🔄 Backend Workflow
The React frontend sends an HTTP request to the Spring Boot backend.
Spring Security checks authentication for protected endpoints.
The JWT authentication filter validates the user's token.
The REST Controller receives the validated request.
The Controller forwards the request to the Service Layer.
The Service Layer performs the required business logic.
The Repository Layer communicates with the MySQL database using Spring Data JPA.
The backend returns the response to the React frontend.
For tourist attractions, the backend communicates with the Geoapify API.
Users can open selected attractions or directions using Google Maps.
🔑 Authentication Flow
User
  ↓
Register / Login
  ↓
Spring Boot Authentication API
  ↓
Credential Verification
  ↓
JWT Token Generation
  ↓
Token Returned to Frontend
  ↓
JWT Sent With Protected Requests
  ↓
Spring Security Validation
  ↓
Access Protected Resources
📁 Project Structure
TravelFlow/
│
├── src/
│   └── main/
│       ├── java/
│       │   └── com/travelflow/TravelFlow/
│       │       ├── controller/
│       │       ├── dto/
│       │       ├── entity/
│       │       ├── repository/
│       │       ├── security/
│       │       ├── service/
│       │       └── TravelFlowApplication.java
│       │
│       └── resources/
│           └── application.properties
│
├── frontend/
│   ├── src/
│   ├── package.json
│   └── vite.config.js
│
├── pom.xml
├── mvnw
├── mvnw.cmd
├── .gitignore
└── README.md
🔌 REST API Endpoints
Authentication
POST /api/auth/register
POST /api/auth/login
GET  /api/protected
Trips
POST   /api/trips
GET    /api/trips
PUT    /api/trips/{id}
DELETE /api/trips/{id}
Itineraries
POST   /api/trips/{tripId}/itineraries
GET    /api/trips/{tripId}/itineraries
PUT    /api/trips/{tripId}/itineraries/{itineraryId}
DELETE /api/trips/{tripId}/itineraries/{itineraryId}
Expenses
POST   /api/trips/{tripId}/expenses
GET    /api/trips/{tripId}/expenses
PUT    /api/trips/{tripId}/expenses/{expenseId}
DELETE /api/trips/{tripId}/expenses/{expenseId}
Budget Summary
GET /api/trips/{tripId}/budget-summary
Dashboard
GET /api/dashboard
Attractions
GET /api/places/destination-attractions?destination={destination}
⚙️ Installation and Setup
Prerequisites
Java 21 or later
Maven
MySQL
Node.js
npm
Git
Clone the Repository
git clone https://github.com/kalletivansh/TravelFlow.git
cd TravelFlow
Create the Database
CREATE DATABASE travelflow;
Environment Variables
TravelFlow uses environment variables for sensitive configuration.

DB_USERNAME
DB_PASSWORD
GEOAPIFY_API_KEY
On Windows:

setx DB_USERNAME "your_mysql_username"
setx DB_PASSWORD "your_mysql_password"
setx GEOAPIFY_API_KEY "your_geoapify_api_key"
Open a new terminal after setting the variables.

Run the Backend
From the TravelFlow root directory:

mvn spring-boot:run
Backend:

http://localhost:8080
Run the Frontend
Open another terminal:

cd frontend
npm install
npm run dev
Frontend:

http://localhost:5173
📱 Application Flow
Home
  ↓
Register / Login
  ↓
Dashboard
  ↓
Trips
  ↓
Create / Select Trip
  ↓
Manage Trip
  ├── Itinerary Management
  ├── Expense Management
  ├── Budget Tracking
  └── Attraction Discovery
            ↓
       Google Maps
🔒 Security
TravelFlow follows secure configuration practices:

JWT-based authentication
Spring Security for protected APIs
Passwords and API keys are not stored directly in the public repository
Environment variables are used for database credentials
Environment variables are used for the Geoapify API key
Protected frontend routes prevent unauthorized access
🔮 Future Enhancements
AI-based personalized itinerary recommendations
Hotel and flight integration
Weather information
Collaborative trip planning
Trip sharing
Advanced expense analytics
Travel notifications
Mobile application
Real-time travel alerts
👨‍💻 Developer
Kalleti Vamshi
B.Tech – Computer Science and Engineering
Anurag University
2024–2028

📚 Project Purpose
TravelFlow was developed as a full-stack Java academic project to demonstrate the practical implementation of:

Full-stack web development
Java and Spring Boot
React frontend development
REST API development
MySQL database integration
Spring Security
JWT authentication
External API integration
Git and GitHub
Trip and itinerary management
Expense and budget management
⭐ TravelFlow
Plan. Organize. Explore.
