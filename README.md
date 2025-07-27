# Fill-It: Smart Container Fullfillment Platform

Full-stack ride-sharing solution with React Native mobile app and Spring Boot backend API.

## Tech Stack

**Frontend**: React Native 0.79.3, React 19.0.0, TypeScript 5.0.4, React Navigation, Maps, Firebase Auth

**Backend**: Spring Boot 3.5.0, Java 17, Firebase, Google Services, Gradle, Docker

## Quick Start

### Prerequisites
- Node.js 18+, Java 17+, Firebase Project, Google Cloud Project
- Android Studio (Android) / Xcode (iOS)

### Setup
```bash
# Frontend
cd frontend
npm install
npm start
npm run android  # or npm run ios

# Backend
cd backend
./gradlew build
./gradlew bootRun
```

## API Endpoints

### Authentication
```http
POST /api/auth/signup/customer    # Customer registration
POST /api/auth/signup/driver      # Driver registration
POST /api/auth/login              # User login
```

### Trip Management
```http
POST /api/trips/create            # Create trip
POST /api/trips/accept            # Accept trip
POST /api/trips/complete          # Complete trip
GET  /api/trips/by-customer       # Customer trips
GET  /api/trips/by-driver         # Driver trips
```

## Configuration

### Frontend (.env)
```env
FIREBASE_API_KEY=your_api_key
FIREBASE_AUTH_DOMAIN=your_auth_domain
FIREBASE_PROJECT_ID=your_project_id
```

### Backend (application.properties)
```properties
spring.application.name=Fill_It
server.port=8080
firebase.database.url=https://your-project.firebaseio.com
```

## Features

### Customer Features
- Ride booking with location selection
- Real-time driver tracking
- Trip history and analytics
- Secure payments

### Driver Features
- Trip acceptance and management
- Real-time navigation
- Earnings tracking
- Professional profile

## Testing & Deployment

```bash
# Testing
cd frontend && npm test
cd backend && ./gradlew test

# Deployment
cd frontend/android && ./gradlew assembleRelease
cd backend && docker build -t fill-it-backend .
```

## Contributing

1. Fork the repository
2. Create feature branch
3. Commit changes
4. Push to branch
5. Open Pull Request

## License

MIT License

## Contact

- **Email**: info@fill-it.com
- **Website**: [fill-it.com](https://fill-it.com)

---

**Made with ❤️ by the Fill-It Team**
