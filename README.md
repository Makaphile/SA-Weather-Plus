📱 App Overview
SA Weather Plus is a feature-rich Android weather application built with Kotlin that provides accurate weather information for South African cities with advanced notification systems and user-friendly features.

✨ Features
🌤️ Core Features
Real-time Weather Data - Current weather conditions for any South African city

Location-based Weather - Automatic weather updates based on your current location

Multi-language Support - English, isiZulu, and Afrikaans

Offline Mode - Access cached weather data without internet connection

Background Sync - Automatic weather updates every 2 hours

🔔 Notification System
Email Notifications - Welcome emails, login alerts, and weather search reports

Push Notifications - Real-time weather alerts and updates

Live Weather Monitoring - Automatic alerts for weather changes

Extreme Weather Alerts - Heat waves, cold waves, and storm warnings

Rain Alerts - Notifications when rain is detected

🔐 Authentication & Security
Email/Password Authentication - Secure user registration and login

Google Sign-In - One-tap authentication with Google

Encrypted Passwords - Firebase Auth security

Session Management - Secure user sessions with SharedPreferences

🎨 User Experience
Modern UI/UX - Material Design with beautiful weather-themed backgrounds

Recent Searches - Quick access to previously searched cities

Weather-based Backgrounds - Dynamic backgrounds that change with weather conditions

Responsive Design - Optimized for all screen sizes

🛠️ Technical Stack
Frameworks & Libraries
Kotlin - Primary programming language

Android Jetpack - ViewBinding, Lifecycle, WorkManager

Firebase - Authentication, Realtime Database, Cloud Messaging

Retrofit2 - REST API consumption

Google Play Services - Location services, Google Sign-In

Architecture
MVVM Pattern - Model-View-ViewModel architecture

Coroutines - Asynchronous programming

Repository Pattern - Data abstraction layer

📋 Prerequisites
Android Studio Hedgehog or later

JDK 17 or higher

Android SDK 34

Minimum SDK 24 (Android 7.0)

🔧 Installation
1. Clone the Repository
bash
git clone https://github.com/Makaphile/SA-Weather-Plus.git
cd SA-Weather-Plus
2. Firebase Setup
Create a new Firebase project at Firebase Console

Add an Android app to your Firebase project

Download google-services.json and place it in app/ directory

Enable the following Firebase services:

Authentication (Email/Password & Google)

Realtime Database

Cloud Messaging

3. API Keys Configuration
OpenWeatherMap API:

Get your API key from OpenWeatherMap

Replace in MainActivity.kt: OPENWEATHER_API_KEY = "your_api_key_here"

Google Sign-In (Optional):

Configure OAuth 2.0 Client ID in Google Cloud Console

Update strings.xml: <string name="default_web_client_id">your_client_id</string>

4. Build and Run
bash
./gradlew assembleDebug
🎯 Usage
First Time Setup
Launch the application

Create an account or sign in with Google

Allow location permissions for accurate weather data

Configure notification preferences in Settings

Daily Use
View Current Weather: Open the app to see weather for your location

Search Cities: Use the search bar to find weather for any South African city

Receive Alerts: Get notified about weather changes and extreme conditions

Multi-language: Change language in settings (English/isiZulu/Afrikaans)

📁 Project Structure
text
app/src/main/java/com/example/saweatherplus/
├── activities/
│   ├── LoginActivity.kt
│   ├── MainActivity.kt
│   ├── SignupActivity.kt
│   ├── LanguageActivity.kt
│   └── NotificationSettingsActivity.kt
├── model/
│   ├── User.kt
│   ├── WeatherData.kt
│   └── WeatherResponse.kt
├── network/
│   ├── RetrofitClient.kt
│   └── WeatherApiService.kt
├── services/
│   ├── LiveNotificationService.kt
│   └── WeatherMonitoringService.kt
├── utils/
│   ├── SessionManager.kt
│   ├── NotificationHelper.kt
│   ├── EmailNotificationService.kt
│   └── WorkManagerHelper.kt
└── workers/
    └── WeatherSyncWorker.kt
🔐 Security Features
Firebase Authentication with encrypted passwords

Secure session management using SharedPreferences

Email verification for account security

Secure API key storage

Location permission handling

🌍 Multi-language Support
The app supports three official South African languages:

English (Default)

isiZulu

Afrikaans

Language switching is available in the Settings menu.

📧 Email Notifications
The app sends automatic email notifications for:

Welcome messages after signup

Security alerts for logins

Weather search reports

Can be disabled in notification settings

🔄 Background Services
WeatherSyncWorker: Syncs weather data every 2 hours

WeatherMonitoringService: Monitors weather changes every 15 minutes

LiveNotificationService: Handles FCM push notifications

🧪 Testing
Unit Tests
bash
./gradlew test
Instrumentation Tests
bash
./gradlew connectedAndroidTest
Test Coverage
bash
./gradlew jacocoTestReport
📊 Performance
Offline First: Caches weather data for offline access

Background Optimized: Efficient background sync with WorkManager

Memory Efficient: Proper lifecycle management

Battery Friendly: Optimized location and network usage

🐛 Troubleshooting
Common Issues
Build Failures

Ensure all API keys are properly configured

Check Firebase configuration

Verify Google Play Services availability

Location Not Working

Enable location permissions

Check device location settings

Verify GPS signal

Notifications Not Received

Check notification permissions

Verify FCM configuration

Review notification settings in app

Logging
Enable debug logging by filtering for "SAWeatherPlus" tag in Logcat.

🤝 Contributing
We welcome contributions! Please follow these steps:

Fork the repository

Create a feature branch: git checkout -b feature/amazing-feature

Commit your changes: git commit -m 'Add amazing feature'

Push to the branch: git push origin feature/amazing-feature

Open a Pull Request

Contribution Guidelines
Follow Kotlin coding conventions

Write unit tests for new features

Update documentation accordingly

Ensure all tests pass before submitting PR

📄 License
This project is licensed under the MIT License - see the LICENSE.md file for details.

🙏 Acknowledgments
OpenWeatherMap for weather data API

Firebase for backend services

Google for Android platform and libraries

Material Design for UI components
