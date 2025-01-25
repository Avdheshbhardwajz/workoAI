# Candidate Referral Portal

A full-stack application for managing candidate referrals.

## Features

- User authentication (login/register)
- Create new referrals with candidate details and resume upload
- View all referrals and their current status
- Update referral status (New, Evaluated, Hired, Rejected)

## Backend Setup

1. Install dependencies:
```bash
cd backend
npm install
```

2. Create a `.env` file in the backend directory using `.env.example` as a template:
```bash
cp .env.example .env
```

3. Update the `.env` file with your configuration:
- Set `MONGODB_URI` to your MongoDB connection string
- Set `JWT_SECRET` to a secure random string
- Optionally change the `PORT` (defaults to 5000)

4. Create uploads directory:
```bash
mkdir uploads
```

5. Run the development server:
```bash
npm run dev
```

## API Endpoints

### Authentication
- POST `/api/auth/register` - Register a new user
- POST `/api/auth/login` - Login user

### Referrals
- POST `/api/referrals` - Create new referral
- GET `/api/referrals` - Get all referrals
- PATCH `/api/referrals/:id/status` - Update referral status

### File Upload
- POST `/api/upload` - Upload resume file

## Frontend Setup (Coming Soon)

The frontend will be built with React and will include:
- Modern UI with a CSS framework
- Responsive design
- Form validation
- File upload functionality
- Real-time status updates
