# 🎬 React Native Movie App

A beautiful and responsive mobile movie discovery app built with **React Native (Expo)**, **TypeScript**, and **NativeWind (Tailwind CSS for React Native)**. This app fetches movie data using the **TMDb API**, showcasing trending and popular movies with full search functionality and a modern, clean UI.

---

## 🚀 Features

- 🔥 **Trending & Popular Movies** – Real-time data using TMDb API  
- 🔎 **Search Functionality** – Instant movie lookup with API integration  
- 🧩 **Reusable Components** – Custom `MovieCard`, `TrendingCard`, and `SearchBar`  
- 📱 **Responsive Layout** – Scrollable UI using `ScrollView` and `FlatList`  
- 🎨 **Gradient Effects** – Stylish visuals using `react-native-linear-gradient`  
- 📦 **Clean Architecture** – Modular file structure for easy maintenance

---

## 🧰 Tech Stack

- [Expo](https://expo.dev/)  
- [React Native](https://reactnative.dev/)  
- [TypeScript](https://www.typescriptlang.org/)  
- [NativeWind (Tailwind CSS)](https://www.nativewind.dev/)  
- [TMDb API](https://developers.themoviedb.org/)  
- [React Navigation](https://reactnavigation.org/)  
- [Axios](https://axios-http.com/) or native `fetch`

---

## 📦 Installation

### Prerequisites

- Node.js and npm  
- Git  
- Expo CLI (`npm install -g expo-cli`)

### Setup

```bash
cd react-native-movie-app
npm install
cp .env.example .env
```

### Add your TMDb API key

Edit the `.env` file:

```env
EXPO_PUBLIC_MOVIE_API_KEY=your_tmdb_api_key_here
```

---

## ▶️ Running the App

```bash
expo start
```

- Use the QR code on your Expo Go app (Android/iOS)  
- Or run on emulator/simulator

---

## 🧭 Project Structure

```
/src
  /components
    MovieCard.tsx
    TrendingCard.tsx
    SearchBar.tsx
  /screens
    HomeScreen.tsx
    SearchScreen.tsx
  /services
    api.ts
  App.tsx
tailwind.config.js
babel.config.js
.env.example
```

---

## 🧱 Key Components

### `SearchBar.tsx`

- Controlled input field  
- Uses debounced API calls to avoid rate limits

### `MovieCard.tsx` / `TrendingCard.tsx`

- Display movie poster, title, rating  
- Responsive design using NativeWind

### `api.ts`

- Manages all TMDb API requests  
- Easy-to-extend endpoints

---

## 💡 Sample Code

### Fetching Movies (api.ts)

```ts
const API_URL = 'https://api.themoviedb.org/3';
const API_KEY = process.env.EXPO_PUBLIC_MOVIE_API_KEY;

export const fetchTrendingMovies = async () => {
  const res = await fetch(`${API_URL}/trending/movie/day?api_key=${API_KEY}`);
  return res.json();
};
```

---

## 🧪 Challenges Faced

- **Search Debounce:** Solved with `setTimeout` to reduce API hits  
- **Responsive Layouts:** Tailwind helped manage layouts using `flex`, `gap`, `h-full`  
- **Loading States:** Added loading spinners and fallback UI

---

## 🛠️ Potential Improvements

- Add **Redux Toolkit** or **Context API** for global state  
- Add **Movie Details Screen** for more info  
- Implement **Caching with AsyncStorage**  
- Add **Unit Tests** with Jest or React Native Testing Library  
- Offline Mode for browsing saved data

---


## 🙌 Acknowledgments

- [TMDb](https://www.themoviedb.org/) for the amazing free movie API  
- [NativeWind](https://www.nativewind.dev/) for Tailwind-like styling in React Native  
- [JavaScript Mastery](https://www.jsmastery.pro/) for open educational content

