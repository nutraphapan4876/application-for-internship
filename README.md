# application-for-internship

Internship application management system

## Setup

### Backend
```bash
cd backend
npm install
npm start
```
Server runs on http://localhost:3000

### Frontend
```bash
cd frontend
npm install
npm start
```
App runs on http://localhost:5173

Database Setup

```sql
CREATE TABLE informations (
   id INT AUTO_INCREMENT PRIMARY KEY,
   full_name VARCHAR(100) NOT NULL,
   uni VARCHAR(100) NOT NULL,
   major VARCHAR(100) NOT NULL,
   email VARCHAR(100) UNIQUE NOT NULL,
   phone VARCHAR(20) NOT NULL,
   start_date DATE NOT NULL,
   end_date DATE NOT NULL,
   skills JSON NOT NULL,
   short_intro TEXT
);
ALTER TABLE informations ADD COLUMN status VARCHAR(50) DEFAULT 'New';
ALTER TABLE informations ADD COLUMN created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP;
```

Features
- Apply for internship
- Admin login & manage applications
- Change applicant status (New, Interview, Accepted, Rejected)
- View applicant details

Tech Stack
- Frontend: React + React Router + Axios
- Backend: Node.js + Express + MySQL
- Database: MySQL
