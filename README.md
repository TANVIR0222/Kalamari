# 🍽️ Kalamari - Food Discovery & Social Sharing Platform

<div align="center">

![Kalamari Logo](./assets/images/iPhone 6.9/iPhone 6.9 - 1.0.png)

**Share your taste. Discover amazing food.**

A modern React Native mobile application for food enthusiasts to discover, share, and connect over their favorite culinary experiences.

**React Native 0.79.2 • Expo 53.0.9 • MIT License**

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
- [Environment Variables](#-environment-variables)
- [Running the App](#-running-the-app)
- [Building for Production](#-building-for-production)
- [Screenshots](#-screenshots)
- [Contributing](#-contributing)
- [License](#-license)
- [Author](#-author)

---

## 🌟 Overview

**Kalamari** is a social platform designed for food lovers to share their culinary adventures, discover new restaurants, and connect with fellow food enthusiasts. Whether you're a home chef, a restaurant explorer, or simply someone who loves good food, Kalamari provides the perfect platform to share your taste and discover amazing dining experiences.

The app combines social networking features with location-based discovery, allowing users to:
- Share food photos and experiences
- Discover restaurants on an interactive map
- Follow other food enthusiasts
- Bookmark favorite posts and recipes
- Rate and review dining experiences

---

## ✨ Features

### 🔐 Authentication & User Management
- **Email & Phone Authentication** - Secure sign-up and login with email or phone number
- **OTP Verification** - Two-factor authentication for enhanced security
- **Password Reset** - Easy password recovery flow
- **Profile Management** - Customizable user profiles with photos and bio

### 📱 Social Features
- **Post Creation** - Share food photos with descriptions, locations, and tags
- **Social Feed** - Browse posts from users you follow
- **User Discovery** - Find and follow other food enthusiasts
- **Comments & Replies** - Engage with posts through threaded comments
- **Bookmarks** - Save your favorite posts for later
- **User Tagging** - Tag other users in your posts

### 🗺️ Location & Discovery
- **Interactive Map** - Discover restaurants and food spots on Google Maps
- **Location Search** - Find places by name or address
- **Directions** - Get directions to your favorite spots
- **Location-based Posts** - See posts from specific restaurants or areas

### 📸 Media & Content
- **Camera Integration** - Take photos directly in the app
- **Photo Gallery** - Access and upload photos from your device
- **Image Picker** - Select multiple photos for posts
- **Media Library** - Manage your uploaded content

### 🔔 Notifications
- **Real-time Notifications** - Stay updated on likes, comments, and follows
- **Notification Center** - View all your notifications in one place

### 🎨 User Experience
- **Dark Mode Support** - Automatic theme switching
- **Smooth Animations** - Powered by React Native Reanimated
- **Bottom Sheets** - Intuitive modal interactions
- **Pull-to-Refresh** - Easy content updates
- **Haptic Feedback** - Enhanced touch interactions

### 🛡️ Safety & Privacy
- **User Blocking** - Block unwanted users
- **Report System** - Report inappropriate content
- **Privacy Settings** - Control your profile visibility
- **Terms & Conditions** - Clear usage guidelines
- **Privacy Policy** - Transparent data handling

---

## 🛠️ Tech Stack

### Core Framework
- **React Native** `0.79.2` - Cross-platform mobile development
- **Expo** `53.0.9` - Development platform and tooling
- **Expo Router** `5.0.6` - File-based routing

### State Management
- **Redux Toolkit** `2.8.2` - State management
- **RTK Query** - Data fetching and caching
- **React Redux** `9.2.0` - React bindings for Redux

### UI & Styling
- **NativeWind (Tailwind CSS)** `4.7.0` - Utility-first styling
- **React Native Paper** `5.14.1` - Material Design components
- **React Native Reanimated** `3.17.4` - Animations
- **React Native SVG** `15.11.2` - SVG support
- **Expo Vector Icons** `14.1.0` - Icon library

### Maps & Location
- **Expo Maps** `0.10.0` - Google Maps & Apple Maps
- **Expo Location** `18.1.5` - Geolocation services
- **@mapbox/polyline** `1.2.1` - Route polyline decoding

### Navigation
- **React Navigation** `7.1.6` - Navigation framework
- **Bottom Tabs** `7.3.10` - Tab navigation
- **Drawer Navigator** `7.3.11` - Side menu navigation

### Media & Camera
- **Expo Camera** `16.1.6` - Camera access
- **Expo Image Picker** `16.1.4` - Photo selection
- **Expo Image** `2.1.7` - Optimized image component
- **Expo Media Library** `17.1.6` - Media access

### Forms & Validation
- **Formik** `2.4.6` - Form management
- **Yup** `1.6.1` - Schema validation

### Storage & Data
- **React Native MMKV** `3.3.0` - Fast key-value storage
- **Axios** `1.9.0` - HTTP client

### Additional Libraries
- **React Native Gesture Handler** `2.24.0` - Touch handling
- **React Native Safe Area Context** `5.4.0` - Safe area handling
- **React Native Share** `12.1.0` - Native sharing
- **React Native WebView** `13.13.5` - WebView component
- **Expo Haptics** `14.1.4` - Haptic feedback
- **use-debounce** `10.0.5` - Debounce hooks

### Development Tools
- **TypeScript** `5.8.3` - Type safety
- **ESLint** `9.25.0` - Code linting
- **Babel** `7.25.2` - JavaScript compiler

---

## 📁 Project Structure

```
kalamari-mobileApp/
├── src/
│   ├── app/                          # Expo Router pages (file-based routing)
│   │   ├── (drawer)/                 # Drawer navigation group
│   │   │   ├── (tab)/                # Tab navigation group
│   │   │   │   ├── index.jsx         # Home/Feed screen
│   │   │   │   ├── Post.jsx          # Create post screen
│   │   │   │   ├── Profile.jsx       # User profile screen
│   │   │   │   ├── Bookmarks.jsx     # Saved posts screen
│   │   │   │   └── _layout.jsx       # Tab layout configuration
│   │   │   ├── ChangePassword.jsx    # Password change screen
│   │   │   ├── Faq.jsx               # FAQ screen
│   │   │   ├── Mission.jsx           # Mission statement
│   │   │   ├── PrivacyPolicy.jsx     # Privacy policy
│   │   │   ├── TermsAndConditions.jsx # Terms of service
│   │   │   └── _layout.jsx           # Drawer layout
│   │   ├── auth/                     # Authentication screens
│   │   │   ├── index.jsx             # Login screen
│   │   │   ├── SingUp.jsx            # Registration screen
│   │   │   ├── phone.jsx             # Phone auth screen
│   │   │   ├── OTPOne.jsx            # OTP verification (email)
│   │   │   ├── OTPVerifyTow.jsx      # OTP verification (phone)
│   │   │   ├── EmailVerify.jsx       # Email verification
│   │   │   ├── ResetPassword.jsx     # Password reset
│   │   │   └── _layout.jsx           # Auth layout
│   │   ├── map/                      # Map & location screens
│   │   │   └── index.jsx             # Map discovery screen
│   │   ├── notifications/            # Notification screens
│   │   ├── randomuser/               # Other user profiles
│   │   ├── searchList/               # Search results
│   │   ├── userSearch/               # User search
│   │   ├── userfollowing/            # Followers/Following lists
│   │   ├── viewpost/                 # Post detail view
│   │   ├── index.tsx                 # Splash screen
│   │   ├── post_details_modal.tsx    # Post modal
│   │   └── _layout.jsx               # Root layout
│   │
│   ├── components/                   # Reusable components
│   │   └── ui/                       # UI components
│   │       ├── AddPhoto.jsx          # Photo upload component
│   │       ├── AlertBox.jsx          # Alert dialogs
│   │       ├── BackButton.jsx        # Navigation back button
│   │       ├── BookMark.jsx          # Bookmark functionality
│   │       ├── ButtomSheet.jsx       # Bottom sheet modals
│   │       ├── CommentSection.jsx    # Comments display
│   │       ├── CustomDrawerContent.jsx # Custom drawer menu
│   │       ├── Header.jsx            # App header
│   │       ├── Location.jsx          # Location picker
│   │       ├── MapView.jsx           # Map component
│   │       ├── PostViewCard.jsx      # Post card component
│   │       ├── ProfileAlert.jsx      # Profile modals
│   │       ├── ReportModal.jsx       # Report functionality
│   │       ├── ShareButton.jsx       # Share functionality
│   │       ├── TabBar.jsx            # Custom tab bar
│   │       ├── TagPepoleView.jsx     # User tagging
│   │       ├── UserCamera.jsx        # Camera component
│   │       ├── UserDiscovery.jsx     # User discovery
│   │       ├── UserPost.jsx          # User posts display
│   │       └── ... (more components)
│   │
│   ├── redux/                        # Redux state management
│   │   ├── api/                      # API configuration
│   │   │   └── baseApi.js            # Base API setup with RTK Query
│   │   ├── apiSlices/                # API slice
│   │   ├── commentApi/               # Comment endpoints
│   │   ├── homeApi/                  # Home feed endpoints
│   │   ├── listApi/                  # List endpoints
│   │   ├── notificationApi/          # Notification endpoints
│   │   ├── postApi/                  # Post endpoints
│   │   ├── profileApi/               # Profile endpoints
│   │   ├── randomuserApi/            # User discovery endpoints
│   │   ├── userReportApi/            # Report endpoints
│   │   └── store.js                  # Redux store configuration
│   │
│   ├── hooks/                        # Custom React hooks
│   ├── lib/                          # Utility libraries
│   │   └── tailwind.js               # Tailwind configuration
│   └── utils/                        # Utility functions
│       └── marker.js                 # Map marker utilities
│
├── assets/                           # Static assets
│   ├── fonts/                        # Custom fonts (Inter, Rubik)
│   ├── images/                       # Images and icons
│   └── Icon.js                       # SVG icon definitions
│
├── android/                          # Android native code
├── .vscode/                          # VS Code configuration
├── app.json                          # Expo configuration
├── babel.config.js                   # Babel configuration
├── tailwind.config.js                # Tailwind CSS configuration
├── tsconfig.json                     # TypeScript configuration
├── package.json                      # Dependencies
├── .env.example                      # Environment variables template
├── .gitignore                        # Git ignore rules
└── README.md                         # This file
```

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v18 or higher)
- **npm** or **yarn** - Package manager (comes with Node.js)
- **Git** - Version control
- **Expo CLI** - Install globally: `npm install -g expo-cli`
- **Android Studio** (for Android development)
- **Xcode** (for iOS development, macOS only)

### Mobile Device or Emulator
- **Expo Go App** (for quick testing on iOS or Android)
- **Android Emulator** (via Android Studio)
- **iOS Simulator** (via Xcode, macOS only)

---

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd kalamari-mobileApp
```

### 2. Install Dependencies

```bash
npm install
# or
yarn install
```

### 3. Set Up Environment Variables

Create a `.env` file in the root directory by copying the example file:

```bash
cp .env.example .env
```

Then edit the `.env` file and add your actual API keys and configuration:

```env
EXPO_PUBLIC_GOOGLE_MAPS_API_KEY=your_actual_google_maps_api_key
EXPO_PUBLIC_API_BASE_URL=http://your-backend-url:8000/api
EXPO_PUBLIC_IMAGE_BASE_URL=http://your-backend-url:8000
```

> **⚠️ Important:** Never commit your `.env` file to version control. It's already included in `.gitignore`.

### 4. Configure Google Maps API Key

#### Get Your API Key
1. Go to Google Cloud Console
2. Create a new project or select an existing one
3. Enable the following APIs:
   - Maps SDK for Android
   - Maps SDK for iOS
   - Places API
   - Directions API
4. Create credentials (API Key)
5. Restrict the API key (recommended for production)

#### Update Configuration
After getting your API key, update:
- `.env` file with your actual key
- `app.json` - Replace `YOUR_GOOGLE_MAPS_API_KEY` with your key

---

## 🔐 Environment Variables

The app uses the following environment variables:

| Variable | Description | Required | Example |
|----------|-------------|----------|---------|
| `EXPO_PUBLIC_GOOGLE_MAPS_API_KEY` | Google Maps API key for maps, places, and directions | Yes | `AIzaSyA...` |
| `EXPO_PUBLIC_API_BASE_URL` | Backend API base URL | Yes | `http://your-backend-url:8000/api` |
| `EXPO_PUBLIC_IMAGE_BASE_URL` | Backend image server URL | Yes | `http://your-backend-url:8000/api` |

### Environment Variable Naming Convention

Expo requires environment variables that need to be accessible in the app to be prefixed with `EXPO_PUBLIC_`. This ensures they are bundled with your app during the build process.

### Security Notes

- ✅ **DO** use `.env.example` as a template (committed to git)
- ✅ **DO** add `.env` to `.gitignore` (already done)
- ❌ **DON'T** commit `.env` with real API keys
- ❌ **DON'T** share API keys publicly
- 🔒 **ALWAYS** restrict API keys in production
- 🔄 **ROTATE** API keys if exposed

---

## 🏃 Running the App

### Development Mode

Start the Expo development server:

```bash
npm start
# or
npx expo start
```

This will open the Expo DevTools in your browser. From here, you can:
- Press `a` to open in Android emulator
- Press `i` to open in iOS simulator
- Scan the QR code with Expo Go app on your physical device

### Platform-Specific Commands

#### Android
```bash
npm run android
# or
npx expo run:android
```

#### iOS (macOS only)
```bash
npm run ios
# or
npx expo run:ios
```

#### Web
```bash
npm run web
# or
npx expo start --web
```

### Clear Cache (if needed)

```bash
npx expo start --clear
```

---

## 📦 Building for Production

### Using EAS Build (Recommended)

1. **Install EAS CLI**
   ```bash
   npm install -g eas-cli
   ```

2. **Login to Expo**
   ```bash
   eas login
   ```

3. **Configure EAS Build**
   ```bash
   eas build:configure
   ```

4. **Build for Android**
   ```bash
   eas build --platform android
   ```

5. **Build for iOS**
   ```bash
   eas build --platform ios
   ```

### Local Builds

#### Android APK
```bash
npx expo build:android -t apk
```

#### Android App Bundle (for Play Store)
```bash
npx expo build:android -t app-bundle
```

#### iOS (requires macOS)
```bash
npx expo build:ios
```

---

## 📸 Screenshots

> **Coming Soon!** Screenshots will be added here to showcase the app's features and user interface.

### Planned Screenshots:
- 🔐 Authentication Flow (Login, Sign Up, OTP)
- 🏠 Home Feed
- 📝 Create Post
- 🗺️ Map Discovery
- 👤 User Profile
- 🔖 Bookmarks
- 💬 Comments & Interactions
- 🔔 Notifications

---

## 🤝 Contributing

We welcome contributions to Kalamari! Here's how you can help:

### Getting Started

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Make your changes**
4. **Commit your changes**
   ```bash
   git commit -m 'Add some amazing feature'
   ```
5. **Push to the branch**
   ```bash
   git push origin feature/amazing-feature
   ```
6. **Open a Pull Request**

### Contribution Guidelines

- Follow the existing code style
- Write clear commit messages
- Add comments for complex logic
- Test your changes thoroughly
- Update documentation as needed
- Ensure no API keys or secrets are committed

### Code Style

- Use ES6+ features
- Follow React/React Native best practices
- Use functional components with hooks
- Keep components small and focused
- Use meaningful variable and function names

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2024 Kalamari Team

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 👨‍💻 Author

**Kalamari Development Team**

- **Organization:** Spark Tech Agency
- **Project:** Kalamari Mobile App

### Contact

- 📧 Email: contact@yourcompany.com
- 🌐 Website: www.yourwebsite.com
- 💼 Social Media: Add your links here

---

## 🙏 Acknowledgments

- **Expo Team** - For the amazing development platform
- **React Native Community** - For the robust framework and ecosystem
- **Google Maps Platform** - For location and mapping services
- **All Contributors** - For making this project better

---

## 📞 Support

If you encounter any issues or have questions:

1. Check the Issues page on your repository
2. Create a new issue with detailed information
3. Contact your development team or support

---

<div align="center">

**Made with ❤️ by the Kalamari Team**

⭐ Star this repo if you find it helpful!

</div>
