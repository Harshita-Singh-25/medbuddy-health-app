# 💊 MedBuddy – Smart Medication Reminder & Health Tracker

A comprehensive full-stack healthcare application built with React and Firebase, designed to help users manage their medication schedules and receive automated email reminders.

## 🌟 Features

### Authentication & Security
- Secure user authentication via Firebase Auth
- Protected routes and persistent login sessions
- User profile management with personalized medication tracking

### Smart Reminder System
- Schedule multiple medication reminders
- Automated email notifications using intelligent cron-based scheduling
- Real-time synchronization with Firebase Firestore database

### Email Automation
- Professional HTML email templates
- Reliable delivery through Nodemailer and Gmail SMTP
- Mobile-responsive email design

### Comprehensive Healthcare Hub
- Home dashboard with overview of medications
- Doctor, pharmacy, and hospital information directory
- User profile with complete medication history
- Privacy policy and terms of service

## 🛠️ Technology Stack

**Frontend**
- React 18 with Vite for fast development
- Tailwind CSS for modern, responsive design
- React Router for seamless navigation
- Firebase SDK for authentication and database

**Backend**
- Node.js with Express.js server
- Automated scheduling with node-cron
- Nodemailer for email service integration
- Environment-based configuration management

**Database**
- Firebase Firestore for real-time data storage
- Scalable NoSQL architecture
- Secure user data management

## 📁 Project Structure

```
MedBuddy/
├── email-server/              # Express.js backend service
│   ├── server.js             # Main server file with cron scheduling
│   └── package.json          # Backend dependencies
├── public/                    # Static assets and favicons
├── src/
│   ├── assets/               # Images, icons, and media files
│   ├── components/           # Reusable UI components
│   │   ├── Navbar.jsx
│   │   └── Footer.jsx
│   ├── pages/                # Application pages
│   │   ├── Home.jsx
│   │   ├── Login.jsx
│   │   ├── Reminder.jsx
│   │   ├── Profile.jsx
│   │   └── [other pages]
│   ├── firebase.js           # Firebase configuration
│   ├── App.jsx               # Main application component
│   └── main.jsx              # Application entry point
├── .env.example              # Environment variables template
├── tailwind.config.js        # Tailwind CSS configuration
├── vite.config.js           # Vite build configuration
└── package.json             # Frontend dependencies
```

## ⚙️ Installation & Setup

### Prerequisites
- Node.js (v16 or higher)
- Firebase project with Firestore enabled
- Gmail account with app password for email service

### Frontend Setup

```bash
# Clone and navigate to project
cd MedBuddy

# Install dependencies
npm install

# Create environment file
cp .env.example .env

# Add your Firebase configuration to .env
# Start development server
npm run dev
```

### Backend Setup

```bash
# Navigate to email server
cd email-server

# Install backend dependencies
npm install

# Create backend environment file
touch .env

# Add email credentials to .env
# Start the email service
npm start
```

### Environment Configuration

**Frontend (.env)**
```env
VITE_FIREBASE_API_KEY=your_firebase_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
VITE_FIREBASE_PROJECT_ID=your_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
VITE_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
VITE_FIREBASE_APP_ID=your_app_id
```

**Backend (email-server/.env)**
```env
GMAIL_USER=your_email@gmail.com
GMAIL_PASS=your_app_password
```

## 🔄 How It Works

The medication reminder system operates through a sophisticated scheduling mechanism:

1. **User Input**: Users add medications with specific timing requirements
2. **Database Storage**: Medication schedules are stored in Firebase Firestore
3. **Automated Monitoring**: Backend cron job checks for due medications every minute
4. **Smart Notifications**: When a medication time matches the current time, the system automatically sends a formatted email reminder
5. **Real-time Updates**: All changes sync across devices in real-time

## 🚀 Deployment

The application is designed for easy deployment on modern platforms:

- **Frontend**: Deploy to Vercel, Netlify, or Firebase Hosting
- **Backend**: Deploy to Railway, Render, or any Node.js hosting service
- **Database**: Firebase Firestore provides automatic scaling and global availability

## 📧 Contact & Support

**Developer**: Harshita Singh    
**GitHub**: [github.com/Harshita-Singh-25](https://github.com/Harshita-Singh-25)

## 🤝 Acknowledgments

This project was originally developed as part of a collaborative hackathon effort. I'd like to acknowledge my project collaborators:

- **Original Team Repository**: [MedBuddy Team Project](https://github.com/Vaishnavii-01/MedBuddy)

**Team Members:**
- **Team Lead & Backend Developer**: Harshita Singh
- **Backend Developer**: Vaishnavi Avhad
- **Frontend Developer**: Bhoomi Naik
- **Frontend Developer**: Manaswi Kabadi

---

*Built with ❤️ to make healthcare management more accessible and reliable.*
