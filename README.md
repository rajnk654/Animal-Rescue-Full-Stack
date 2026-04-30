🐾 Animal Rescue Full Stack Application

Welcome to the Animal Rescue and Adoption Full Stack Web Application!
This project combines a Spring Boot backend and a ReactJS frontend to deliver a complete platform for animal rescue, adoption, foster care, and donations.

📌 Project Overview

The Animal Rescue Full Stack Application is designed to digitalize and streamline animal welfare operations—from rescuing stray animals to managing adoptions and donations.

It provides:

🐶 A centralized system for managing animal records
🏠 Seamless adoption & foster workflows
👩‍⚕️ Tools for rescuers and admins
💳 Secure donation & payment processing
🌐 A modern, responsive user interface

🧩 Architecture
Animal-Rescue-Full-Stack/
│
├── backend/    → Spring Boot REST API
└── frontend/   → ReactJS Web Application

🛠 Backend (Spring Boot)
🚀 Features
Role-Based Access Control (Adopter, Rescuer, Admin)
JWT Authentication & Authorization
Pet Listings with Search & Filters
Adoption Workflow Management
Foster Care Tracking
Payment Integration (Stripe / Razorpay)
RESTful APIs with Validation
Scalable MVC Architecture

🧰 Tech Stack
Framework: Spring Boot
Database: PostgreSQL
ORM: Hibernate / JPA
Security: Spring Security + JWT
Build Tool: Maven
Payments: Stripe / Razorpay

📂 Backend Structure
backend/
 ├── controller/
 ├── model/
 ├── repository/
 ├── service/
 ├── config/
 ├── dto/
 └── resources/
 
 ⚙️ Backend Setup
1️⃣ Prerequisites
Java 17+
Maven
PostgreSQL
Git

2️⃣ Installation
git clone <repo-url>
cd backend
git checkout master

3️⃣ Configuration

Edit application.properties:

spring.datasource.url=jdbc:postgresql://localhost:5432/animalrescue
spring.datasource.username=postgres
spring.datasource.password=yourpassword

spring.jpa.hibernate.ddl-auto=update

payment.key=your_key
payment.secret=your_secret

4️⃣ Run Backend
mvn clean install
mvn spring-boot:run

Backend runs at:
👉 http://localhost:8080

📡 Backend APIs
Authentication
POST /api/auth/register
POST /api/auth/login

Pets
GET /api/pets
POST /api/pets
PUT /api/pets/{id}
DELETE /api/pets/{id}

Adoption
POST /api/adoptions/apply
GET /api/adoptions/status
Foster Care
GET /api/foster
POST /api/foster

Payments
POST /api/payments/initiate
POST /api/payments/donation

🎨 Frontend (ReactJS)
🚀 Features
Google Authentication (OAuth 2.0)
Google reCAPTCHA (v2/v3)
Role-Based UI
Advanced Pet Search
Adoption Tracking UI
Foster Care Interface
Secure Payment Integration
Mobile Responsive Design

🧰 Tech Stack
Framework: ReactJS
Routing: React Router DOM
State Management: Context API / Redux
Auth: Google OAuth
Payments: Stripe / Razorpay
HTTP: Axios / Fetch
Styling: CSS / Bootstrap / Tailwind

📂 Frontend Structure
frontend/
 ├── components/
 ├── pages/
 ├── services/
 ├── context/
 ├── App.js
 └── index.js

 ⚙️ Frontend Setup
1️⃣ Prerequisites
Node.js (v16+)
Yarn / npm
Git

2️⃣ Installation
cd frontend
git checkout master
yarn install

3️⃣ Environment Variables

Create .env:
REACT_APP_API_BASE_URL=http://localhost:8080
REACT_APP_PAYMENT_KEY=your_payment_key
REACT_APP_GOOGLE_CLIENT_ID=your_google_client_id
REACT_APP_RECAPTCHA_SITE_KEY=your_recaptcha_key

4️⃣ Run Frontend
yarn start

Frontend runs at:
👉 http://localhost:3000

🔐 Integrations
Google OAuth Setup
Configure OAuth in Google Cloud Console
Add localhost:3000 as authorized origin
Add Client ID to .env

reCAPTCHA Setup
Register site in Google reCAPTCHA
Add Site Key in frontend
Verify using backend secret key

Stripe / Razorpay
Add public key in frontend .env
Add secret key in backend

Flow:
Frontend → Backend → Payment Gateway → Response

🔄 How Full Stack Works Together
User interacts with React frontend
Frontend sends API requests to backend
Backend processes logic & database operations
Backend returns JSON response
Frontend updates UI

🌟 Use Cases
Animal Shelters & NGOs
Rescue Volunteers
Pet Adopters & Foster Families
Donors supporting animal welfare

🚀 Deployment
Backend
Deploy on: Railway / Render / AWS / Docker
Frontend
yarn build

📄 License

MIT License

📬 Contact

For queries or collaboration:

Open an issue
Reach out to the maintainer

🐶 “Adopt, Don’t Shop” ❤️
