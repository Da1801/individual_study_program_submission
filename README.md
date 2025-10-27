Title: ISP submission system

Description: Applied Computer Science program ISP(Individual Study Program) submission
system revises some functionalities of UCLL’s KuLoket: Student can choose courses based on
their profiles(study points, passed exam), and review his/her ISP.

#  ISP Submission Platform

A full-stack project built with **Next.js**, **Node.js**, and **PostgreSQL**, using **Prisma** ORM and JWT-based authentication.  
This platform allows users to submit, view, and manage ISP-related data through a modern web interface.

---

##  Project Structure
```
root/
│
├── frontend/                # Next.js frontend (React + TypeScript)
│   ├── components/
│   ├── pages/
│   ├── public/
│   └── .env
│
├── backend/                 # Node.js backend (Express + Prisma + PostgreSQL)
│   ├── src/
│   ├── prisma/
│   ├── util/
│   └── .env
│
└── README.md
```

---

##  Getting Started

Follow these steps to set up and run the project locally.

---

###  Frontend Setup

1. Navigate to the frontend directory:
```bash
   cd frontend
```

2. Create a `.env` file inside the frontend directory and add:
```env
   NEXT_PUBLIC_API_URL=http://localhost:3000
```

3. Install dependencies:
```bash
   npm install
```

4. Start the frontend in development mode:
```bash
   npm run dev
```

5. The frontend will now be running at:
```
   http://localhost:8080
```

---

### ⚙️ Backend Setup

1. From the root of the project, navigate to the backend:
```bash
   cd backend
```

2. Create a `.env` file inside the backend directory and add:
```env
   DATABASE_URL="postgresql://postgres:postgres@localhost:5432/isp-submission?schema=public"
   APP_PORT=3000
   JWT_SECRET="d2ViNC1ub3Qtc28tc2VjcmV0LWFjY2Vzcy1zZWNyZXQ="
   JWT_EXPIRES_HOURS=8
```

3. Install backend dependencies:
```bash
   npm install
```

4. Generate the Prisma client:
```bash
   npx prisma generate
```

5. Seed the database (make sure PostgreSQL is running and accessible):
```bash
   npx ts-node util/seed.ts
```

6. Start the backend server:
```bash
   npm start
```

7. The backend API will be available at:
```
   http://localhost:3000
```

---

##  Notes

- Make sure PostgreSQL is installed and running before starting the backend
- Default database credentials are `postgres:postgres` - update these in the `DATABASE_URL` if your setup differs
- The JWT secret provided is for development only - use a secure secret in production
- Frontend and backend run on different ports (8080 and 3000 respectively)

---

##  Technologies Used

- **Frontend**: Next.js, React, TypeScript
- **Backend**: Node.js, Express
- **Database**: PostgreSQL
- **ORM**: Prisma
- **Authentication**: JWT

---

