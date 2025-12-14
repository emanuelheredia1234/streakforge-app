# StreakForge - Complete Project Setup Guide

## 🎯 Overview
StreakForge is a habit-building workout app with gamification, AI-powered adaptive motivation, and comprehensive progress tracking.

## 📋 Prerequisites
- Node.js (v18 or higher)
- npm or yarn
- Expo CLI: `npm install -g expo-cli`
- MongoDB (local or Atlas)
- Git
- Cursor IDE or VS Code

## 🏗️ Project Structure

```
streakforge-app/
├── frontend/                 # React Native (Expo) app
│   ├── src/
│   │   ├── components/      # Reusable UI components
│   │   │   ├── StreakCounter.tsx
│   │   │   ├── FitnessGarden.tsx
│   │   │   ├── WorkoutCard.tsx
│   │   │   └── ProgressChart.tsx
│   │   ├── screens/         # App screens
│   │   │   ├── auth/
│   │   │   │   ├── LoginScreen.tsx
│   │   │   │   └── SignupScreen.tsx
│   │   │   ├── onboarding/
│   │   │   │   ├── GoalsScreen.tsx
│   │   │   │   ├── ScheduleScreen.tsx
│   │   │   │   └── ProfileSetupScreen.tsx
│   │   │   ├── DashboardScreen.tsx
│   │   │   ├── WorkoutsScreen.tsx
│   │   │   ├── GardenScreen.tsx
│   │   │   ├── ProgressScreen.tsx
│   │   │   └── CommunityScreen.tsx
│   │   ├── navigation/
│   │   │   └── AppNavigator.tsx
│   │   ├── store/           # Redux Toolkit
│   │   │   ├── slices/
│   │   │   │   ├── authSlice.ts
│   │   │   │   ├── streakSlice.ts
│   │   │   │   ├── workoutSlice.ts
│   │   │   │   └── gamificationSlice.ts
│   │   │   └── store.ts
│   │   ├── services/
│   │   │   ├── api.ts
│   │   │   ├── firebase.ts
│   │   │   └── notifications.ts
│   │   ├── hooks/
│   │   │   ├── useStreak.ts
│   │   │   └── useWorkout.ts
│   │   ├── utils/
│   │   │   ├── dateHelpers.ts
│   │   │   └── validators.ts
│   │   ├── types/
│   │   │   └── index.ts
│   │   └── assets/
│   ├── App.tsx
│   ├── app.json
│   ├── package.json
│   └── tsconfig.json
│
├── backend/                 # Node.js/Express API
│   ├── src/
│   │   ├── controllers/
│   │   │   ├── authController.ts
│   │   │   ├── workoutController.ts
│   │   │   ├── streakController.ts
│   │   │   └── aiController.ts
│   │   ├── models/
│   │   │   ├── User.ts
│   │   │   ├── Workout.ts
│   │   │   ├── Streak.ts
│   │   │   └── Achievement.ts
│   │   ├── routes/
│   │   │   ├── auth.ts
│   │   │   ├── workouts.ts
│   │   │   ├── streaks.ts
│   │   │   └── ai.ts
│   │   ├── middleware/
│   │   │   ├── auth.ts
│   │   │   └── errorHandler.ts
│   │   ├── services/
│   │   │   ├── aiService.ts
│   │   │   └── notificationService.ts
│   │   ├── config/
│   │   │   └── database.ts
│   │   └── server.ts
│   ├── package.json
│   └── tsconfig.json
│
└── docs/
    ├── API.md
    └── FEATURES.md
```

## 🚀 Quick Start

### 1. Clone Repository
```bash
git clone https://github.com/emanuelheredia1234/streakforge-app.git
cd streakforge-app
```

### 2. Setup Backend
```bash
cd backend
npm install

# Create .env file
cat > .env << EOF
PORT=3000
MONGODB_URI=mongodb://localhost:27017/streakforge
JWT_SECRET=your_jwt_secret_here
OPENAI_API_KEY=your_openai_key_here
FIREBASE_PROJECT_ID=your_firebase_project_id
EOF

# Start development server
npm run dev
```

### 3. Setup Frontend
```bash
cd frontend
npm install

# Create .env file
cat > .env << EOF
API_URL=http://localhost:3000
FIREBASE_API_KEY=your_firebase_api_key
FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
FIREBASE_PROJECT_ID=your_project_id
EOF

# Start Expo
npm start
```

## 🎮 Core Features Implementation

### 1. Authentication System
- Firebase Auth for email/password and social login
- JWT tokens for API authentication
- Secure password hashing with bcrypt

### 2. Gamification Engine
- **Streak System**: Track consecutive workout days
- **Fitness Garden**: Visual representation with plants that grow
- **XP & Levels**: Points system (1-100 levels)
- **Achievements**: Unlock badges for milestones
- **Streak Revival**: 5-minute challenge to recover missed days

### 3. AI Personalization
- OpenAI integration for adaptive messaging
- Mood/energy pattern analysis
- Smart notification timing
- Personalized workout recommendations

### 4. Workout Library
Pre-built workouts by duration:
- 5min: Quick Burst, Desk Stretch
- 10min: HIIT Basics, Core Focus  
- 15min: Full Body Quick, Cardio Blast
- 20min: Strength Essentials
- 30min: Complete Workout

### 5. Community Features
- Anonymous streak feed
- Buddy matching algorithm
- Success stories
- Group challenges

### 6. Progress Tracking
- Daily mood & energy logs
- Strength PRs tracker
- Progress photos
- Body measurements
- Weekly insights

### 7. Freemium Model
**Free Tier:**
- Basic streaks
- 5-15min workouts
- Basic notifications
- Ads

**Premium ($9.99/month):**
- Full workout library
- Advanced AI coaching
- Custom plans
- Calendar integration
- Ad-free
- Advanced analytics

## 📱 Development with Cursor IDE

### Using Cursor AI Features

1. **Open project in Cursor Desktop**
```bash
cursor .
```

2. **Use Cursor Chat (Cmd/Ctrl+L)**
- Ask: "Create the StreakCounter component with animations"
- Ask: "Generate MongoDB schema for User model with streaks"
- Ask: "Implement the gamification logic for XP points"

3. **Use Cursor Composer (Cmd/Ctrl+I)**
- Select multiple files and ask for cross-file changes
- Request: "Add TypeScript types across all components"

4. **Use Tab Autocomplete**
- Cursor will suggest code as you type
- Accept with Tab key

## 🔧 Next Steps

### Phase 1: Foundation (Week 1-2)
1. ✅ Set up project structure
2. ⬜ Implement authentication
3. ⬜ Create basic navigation
4. ⬜ Set up MongoDB schemas

### Phase 2: Core Features (Week 3-4)
5. ⬜ Build streak tracking system
6. ⬜ Create workout library
7. ⬜ Implement dashboard UI

### Phase 3: Gamification (Week 5-6)
8. ⬜ Build fitness garden
9. ⬜ Add XP/leveling system
10. ⬜ Create achievement badges

### Phase 4: AI & Advanced (Week 7-8)
11. ⬜ Integrate OpenAI for coaching
12. ⬜ Implement smart notifications
13. ⬜ Add community features

### Phase 5: Polish & Launch (Week 9-10)
14. ⬜ Implement freemium model
15. ⬜ Testing & bug fixes
16. ⬜ App store preparation

## 📚 Recommended Resources
- [React Native Docs](https://reactnative.dev/)
- [Expo Documentation](https://docs.expo.dev/)
- [MongoDB Manual](https://docs.mongodb.com/)
- [OpenAI API Docs](https://platform.openai.com/docs)
- [Firebase Auth Guide](https://firebase.google.com/docs/auth)

## 🤝 Contributing
This is a personal project. For major changes, please create an issue first.

## 📄 License
MIT License - see LICENSE file

## 🎯 Vision
To create the most engaging fitness habit app that helps users build sustainable workout routines through psychology-backed gamification and AI-powered motivation.

---

**Created by:** Emanuel Heredia  
**Date:** December 2025  
**Status:** In Development
