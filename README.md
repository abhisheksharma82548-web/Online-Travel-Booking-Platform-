TravelQuest 🌍✈️

TravelQuest is a modern, full-stack, AI-powered travel booking platform. It allows users to discover destinations, receive AI-powered recommendations, manage bookings, view personalized dashboards, and provides an admin dashboard for managing bookings and destinations. The project is built using Next.js, Tailwind CSS, Prisma, OpenAI, Mapbox, and NextAuth.

Features ✅
User Features

🔎 Search Destinations: Search for travel locations by name, climate, or budget.

🤖 AI Recommendations: Personalized destination suggestions using OpenAI GPT-4.

🗺️ Interactive Map: View locations with Mapbox integration.

💳 Booking System: Real bookings stored in a database (Prisma + SQLite/Postgres).

👤 User Dashboard: View all personal bookings.

❤️ Favorites Dashboard: Save favorite destinations for easy access.

Admin Features

🧑‍💼 Admin Dashboard: View all user bookings in a table.

📝 Destination Management: Add new destinations to the system.

🔒 Authentication & Roles: Secure login using NextAuth with Google.

Technical Features

⚡ Next.js 14 (App Router): Modern React framework for SSR/SSG.

🎨 Tailwind CSS: Responsive, mobile-first UI styling.

🗄️ Prisma ORM: Database management for bookings and admin features.

🧠 OpenAI GPT-4: AI-powered recommendations.

📍 Mapbox: Real-time maps and geolocation.

🔐 NextAuth.js: Secure authentication using OAuth providers.

Tech Stack 🛠️
Layer	Technology
Frontend	Next.js 14 (App Router), React
Styling	Tailwind CSS
AI	OpenAI GPT-4
Auth	NextAuth.js (Google)
Database	Prisma + SQLite / Postgres
Maps	Mapbox GL JS
API	Next.js API routes
Deployment	Vercel
Folder Structure 📂
travelquest/
├─ app/
│  ├─ layout.tsx              # Global layout (Navbar, body)
│  ├─ page.tsx                # Home page
│  ├─ dashboard/page.tsx      # User bookings dashboard
│  ├─ admin/page.tsx          # Admin dashboard
│  ├─ api/
│  │  ├─ ai/route.ts          # AI recommendations API
│  │  ├─ destinations/route.ts# Fetch travel destinations (Amadeus API)
│  │  ├─ bookings/route.ts    # Bookings CRUD API
│  │  └─ auth/[...nextauth]/route.ts # Authentication API
├─ components/
│  ├─ Navbar.tsx
│  ├─ DestinationCard.tsx
│  ├─ SearchBar.tsx
│  ├─ MapView.tsx
│  └─ AdminForm.tsx
├─ lib/
│  ├─ prisma.ts               # Prisma client
│  ├─ openai.ts               # OpenAI API client
│  └─ amadeus.ts              # Amadeus Travel API client
├─ prisma/
│  └─ schema.prisma           # Prisma schema
├─ styles/
│  └─ globals.css             # Tailwind global styles
├─ .env.local                 # Environment variables
└─ package.json

Installation & Setup ⚡

Clone the repository

git clone https://github.com/yourusername/travelquest.git
cd travelquest


Install dependencies

npm install


Setup environment variables
Create a .env.local file with the following:

OPENAI_API_KEY=your_openai_key
AMADEUS_CLIENT_ID=your_amadeus_id
AMADEUS_CLIENT_SECRET=your_amadeus_secret
NEXTAUTH_SECRET=supersecret
GOOGLE_ID=your_google_id
GOOGLE_SECRET=your_google_secret
DATABASE_URL="file:./dev.db"   # Or Postgres URL for production
NEXT_PUBLIC_MAPBOX_TOKEN=your_mapbox_token


Setup Prisma Database

npx prisma migrate dev --name init


Run the development server

npm run dev


Open your browser

http://localhost:3000

Usage 🚀

Login using Google authentication.

Search destinations or get AI recommendations.

Add to favorites or book destinations.

Admin Dashboard (for admins):

View all bookings.

Add new destinations.

APIs Used 🌐

Amadeus Travel API – fetch destination and travel data.

OpenAI GPT-4 – AI-powered travel recommendations.

NextAuth – authentication and session management.

Prisma – database queries for bookings and admin features.

Deployment 🌍

The project can be deployed on Vercel:

npm install -g vercel
vercel


Vercel will automatically detect the Next.js app and deploy it with all APIs.

Future Enhancements 🔮

Stripe integration for real payments.

Email notifications for bookings.

Role-based admin security.

AI itinerary planner (full multi-day suggestions).

Enhanced map features: route planning & geolocation clustering.

Contributing 🤝

Fork the repository.

Create a new branch: git checkout -b feature-name

Commit your changes: git commit -m "Add new feature"

Push to the branch: git push origin feature-name

Open a Pull Request.

License 📄

MIT License © 2025 Your Name
