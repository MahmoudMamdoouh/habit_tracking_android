# 🌱 Habit Tracking Android

A modern Android habit tracking application that helps users build and maintain daily habits using Firebase Authentication and Firebase Realtime Database.

## ✨ Features

- User authentication with email and password
- Real-time habit tracking
- Add daily habits
- Mark habits as completed for the day
- Secure user data with Firebase authentication
- Responsive and intuitive UI design

## 🏗️ Technical Architecture

### Architecture Overview

The application follows Clean Architecture principles with MVVM pattern, ensuring:

- Clear separation of concerns
- High testability
- Scalable and maintainable codebase
- Unidirectional data flow

### Key Technical Decisions

#### UI Layer

- **Navigation Component**: Type-safe navigation between fragments
- **Material Design**: Modern design guidelines
- **MVVM Pattern**: Separation of UI logic and data
- **View Binding**: Efficient view interactions

#### Domain Layer

- **Use Cases**: Encapsulated business logic
- **Single Responsibility Principle**: Modular code design

## 🔄 Trade-offs & Decisions

1. **Authentication Strategy**

   - Chose email/password authentication for simplicity
   - Implemented robust validation and error handling

2. **Data Persistence**

   - Leveraged Firebase Realtime Database for instant updates
   - Implemented strict security rules for user data privacy

3. **UI Implementation**
   - Used Android Fragments for modular UI components
   - Implemented responsive design for various screen sizes

## 🔜 Future Improvements

1. **Technical**

   - Implement more authentication methods (Google, Facebook)
   - Add comprehensive unit and integration tests
   - Implement habit streaks and progress tracking

2. **User Experience**
   - Implement habit reminders and notifications
   - Add detailed habit analytics
   - Create custom habit categories

## 🛠️ Setup & Installation

1. Clone the repository
2. Set up Firebase project
   - Create Firebase project
   - Add google-services.json to the app module
3. Configure Firebase Realtime Database security rules
4. Build and run the project

### Firebase Realtime Database Rules

```json
{
  "rules": {
    "habits": {
      "$uid": {
        ".read": "auth !== null && auth.uid === $uid",
        ".write": "auth !== null && auth.uid === $uid"
      }
    }
  }
}
```
