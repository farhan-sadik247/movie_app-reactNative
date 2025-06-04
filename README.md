# MovieTime

A modern React Native mobile application built with Expo that allows users to discover, search, and explore movies. The app features trending movies based on community search patterns, detailed movie information, and a sleek dark-themed interface.

## 📌 Overview

MovieTime is designed to provide movie enthusiasts with an intuitive way to discover new films and get detailed information about their favorites. The app leverages The Movie Database (TMDB) API for comprehensive movie data and uses Appwrite as a backend to track trending searches, creating a community-driven trending system.

Key capabilities include:
- Browse popular movies
- Search through thousands of movies
- View trending movies based on community searches
- Access detailed movie information including cast, budget, and reviews
- Save favorite movies (coming soon)
- User profiles and personalization (coming soon)

Built using **React Native**, **Expo**, **TypeScript**, and **NativeWind**, the application ensures a smooth, native mobile experience across iOS and Android platforms.

## 🚀 Features

- 🎬 **Movie Discovery**  
  Browse popular and latest movies with beautiful poster displays and essential information like ratings and release dates.

- 🔍 **Smart Search**  
  Real-time search functionality with debouncing for optimal performance and user experience.

- 📈 **Community Trending System**  
  Dynamic trending movies section that tracks what the community searches for most. Uses Appwrite database to store search analytics and displays the top 10 most searched movies with animated ranking badges.

- 📱 **Responsive Design**  
  Fully responsive interface optimized for various screen sizes using NativeWind (Tailwind CSS for React Native).

- 🎭 **Detailed Movie Info**  
  Comprehensive movie details including synopsis, cast, budget, revenue, production companies, and user ratings.

- 🌙 **Dark Theme**  
  Beautiful dark-themed interface with purple accent colors for an immersive viewing experience.

- 🚀 **Tab Navigation**  
  Intuitive bottom tab navigation with custom animated tab indicators.

## 🛠️ Tech Stack

- **Frontend** – React Native with Expo
- **Language** – TypeScript
- **Styling** – NativeWind (Tailwind CSS for React Native)
- **Navigation** – Expo Router
- **API** – The Movie Database (TMDB) API
- **Backend** – Appwrite (for trending analytics)
- **State Management** – Custom hooks with React hooks

## 🛠️ Installation Guide

This project requires Node.js and either an iOS simulator, Android emulator, or physical device for testing.

### 📦 Prerequisites

- [Node.js](https://nodejs.org/) (v18 or above recommended)
- [Expo CLI](https://docs.expo.dev/get-started/installation/) 
- [Expo Go](https://expo.dev/client) app on your mobile device (for testing)
- iOS Simulator (Mac only) or Android Studio (for emulators)
- TMDB API key from [The Movie Database](https://www.themoviedb.org/settings/api)
- Appwrite project setup (optional, for trending features)

### 🚀 Local Setup

1. **Clone the Repository**

   ```bash
   $ git clone https://github.com/farhan-sadik247/movie_app-reactNative.git
   $ cd movieApp
   ```

2. **Install Dependencies**

   ```bash
   $ npm install
   ```

3. **Environment Setup**

   Create a `.env` file in the root directory:

   ```env
   EXPO_PUBLIC_MOVIE_API_KEY=your_tmdb_api_key_here
   EXPO_PUBLIC_APPWRITE_PROJECT_ID=your_appwrite_project_id
   EXPO_PUBLIC_APPWRITE_DATABASE_ID=your_appwrite_database_id
   EXPO_PUBLIC_APPWRITE_COLLECTION_ID=your_appwrite_collection_id
   ```

4. **Start the Development Server**

   ```bash
   $ npx expo start
   ```

5. **Run on Device/Emulator**

   - **Physical Device**: Scan the QR code with Expo Go app
   - **iOS Simulator**: Press `i` in the terminal
   - **Android Emulator**: Press `a` in the terminal

## 📱 App Structure

```
app/
├── (tabs)/                 # Tab navigation screens
│   ├── index.tsx          # Home screen with trending and popular movies
│   ├── search.tsx         # Search functionality
│   ├── saved.tsx          # Saved movies (placeholder)
│   └── profile.tsx        # User profile (placeholder)
├── movies/[id].tsx        # Dynamic movie details screen
└── _layout.tsx            # Root layout configuration

components/
├── MovieCard.tsx          # Reusable movie card component
├── TrendingCard.tsx       # Trending movie card with ranking
└── SearchBar.tsx          # Search input component

services/
├── api.ts                 # TMDB API integration
├── appwrite.ts            # Appwrite backend services
└── useFetch.ts            # Custom hook for data fetching
```

## 🎨 Design Features

- **Custom Tab Bar**: Animated tab bar with highlight effects
- **Gradient Rankings**: Masked gradient numbers for trending movies
- **Responsive Grid**: Adaptive movie grid layout
- **Loading States**: Smooth loading indicators and error handling
- **Image Optimization**: Optimized poster loading with fallbacks
- **Trending Analytics**: Real-time tracking of search patterns to surface popular movies

## 🔥 Trending System

The app features a sophisticated trending system that analyzes user search behavior:

- **Search Tracking**: Every search query is logged with the selected movie
- **Popularity Ranking**: Movies are ranked by search frequency
- **Real-time Updates**: Trending list updates dynamically based on community activity
- **Visual Indicators**: Gradient-masked ranking numbers (1-10) for trending movies
- **Debounced Analytics**: Search tracking is optimized to avoid spam and ensure accurate data

The trending algorithm prioritizes recent searches while maintaining historical data, creating a balanced view of both current and sustained popularity.

## 🔧 Configuration

### TMDB API Setup
1. Create an account at [TMDB](https://www.themoviedb.org/)
2. Navigate to Settings > API
3. Generate an API key
4. Add the key to your environment variables

### Appwrite Setup (Optional)
1. Create an [Appwrite](https://appwrite.io/) project
2. Set up a database and collection for trending movies
3. Configure the collection with the following attributes for the trending system:
   - `searchTerm` (string) - The search query that led to the movie
   - `movie_id` (integer) - TMDB movie ID
   - `title` (string) - Movie title
   - `count` (integer) - Number of times this movie was searched
   - `poster_url` (string) - Movie poster URL for display

## 🚀 Building for Production

### Android
```bash
$ npx expo build:android
```

### iOS
```bash
$ npx expo build:ios
```

### Using EAS Build (Recommended)
```bash
$ npx eas build --platform all
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [The Movie Database (TMDB)](https://www.themoviedb.org/) for providing the movie data API
- [Expo](https://expo.dev/) for the amazing React Native development platform
- [NativeWind](https://www.nativewind.dev/) for bringing Tailwind CSS to React Native
- [Appwrite](https://appwrite.io/) for backend services
- [JavaScript Mastery](https://www.youtube.com/watch?v=f8Z9JyB2EIE) for basic information about ReactNative
