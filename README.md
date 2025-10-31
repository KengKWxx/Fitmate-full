# FITMAT - Fitness Training Management System

A comprehensive fitness training management platform with backend and frontend built with modern technologies.

## 🚀 Features

- **User Management**: User registration, authentication, and role-based access control
- **Trainer Management**: Trainer profiles, ratings, and reviews
- **Class Management**: Create, update, and manage fitness classes
- **Booking System**: Class enrollment and booking management
- **Payment Integration**: Stripe payment integration for memberships
- **Admin Dashboard**: Comprehensive admin panel for managing all aspects of the platform

## 🛠️ Tech Stack

### Backend
- **Node.js** with **Express.js**
- **TypeScript** for type safety
- **Prisma ORM** with MySQL database
- **JWT** for authentication
- **Stripe** for payment processing

### Frontend
- **Next.js** - React framework
- **TypeScript** for type safety
- **Tailwind CSS** for styling
- **SweetAlert2** for user notifications

## 📁 Project Structure

```
FITMAT/
├── Fitmat-BackEnd/        # Backend API server
│   ├── src/
│   │   ├── controllers/   # Route controllers
│   │   ├── routes/        # API routes
│   │   ├── middleware/    # Authentication middleware
│   │   └── utils/         # Utility functions
│   └── prisma/            # Database schema and migrations
│
└── Fitmat-FrontEnd/       # Frontend Next.js application
    ├── components/        # React components
    ├── src/
    │   ├── pages/         # Next.js pages
    │   └── styles/        # Global styles
    └── public/            # Static assets
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v16 or higher)
- MySQL database
- npm or yarn

### Backend Setup

1. Navigate to backend directory:
```bash
cd Fitmat-BackEnd
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
Create a `.env` file in `Fitmat-BackEnd/`:
```
DATABASE_URL="mysql://user:password@localhost:3306/fitmat"
JWT_SECRET="your-secret-key"
STRIPE_SECRET_KEY="your-stripe-secret-key"
PORT=4000
```

4. Run Prisma migrations:
```bash
npx prisma migrate dev
```

5. Generate Prisma client:
```bash
npx prisma generate
```

6. Start the server:
```bash
npm run dev
```

The backend API will be available at `http://localhost:4000`

### Frontend Setup

1. Navigate to frontend directory:
```bash
cd Fitmat-FrontEnd
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
Create a `.env.local` file in `Fitmat-FrontEnd/`:
```
NEXT_PUBLIC_API_BASE_URL=http://localhost:4000/api
```

4. Start the development server:
```bash
npm run dev
```

The frontend will be available at `http://localhost:3000`

## 📝 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/change-password` - Change password

### Classes
- `GET /api/classes` - List all classes
- `POST /api/classes` - Create new class (Admin only)
- `PUT /api/classes/:classId` - Update class (Admin only)
- `DELETE /api/classes/:classId` - Delete class (Admin only)

### Trainers
- `GET /api/trainers` - List all trainers
- `GET /api/trainers/:trainerId` - Get trainer details

### Reviews
- `GET /api/reviews` - List all reviews
- `POST /api/reviews` - Create review
- `DELETE /api/reviews/:reviewId` - Delete review (Admin only)

### Users
- `GET /api/users` - List all users (Admin only)
- `PUT /api/users/:userId` - Update user profile

## 🎨 Features Overview

### For Users
- Browse and enroll in fitness classes
- View trainer profiles and reviews
- Manage account settings
- Track bookings and class history

### For Trainers
- View assigned classes
- Manage class schedules
- Track student enrollments

### For Admins
- Complete user management
- Class and category management
- Trainer management and promotion
- Review moderation
- Contact request management
- Payment verification

## 🔐 Security

- JWT-based authentication
- Role-based access control (USER, TRAINER, ADMIN)
- Password hashing with bcrypt
- Secure API endpoints with middleware protection

## 📄 License

This project is private and proprietary.

## 👥 Contributing

This is a private project. Please contact the repository owner for contribution guidelines.

## 📞 Support

For issues or questions, please contact the development team.

