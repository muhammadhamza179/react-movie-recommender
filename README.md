🎬 React Movie Recommendation System

A React-based movie recommendation and search application built with a component-based architecture, API integration, and routing. This project demonstrates how to structure React applications while fetching real-world data dynamically from APIs.

🚀 Features

Component-Based Architecture (Navbar, MovieCard, Search, Favorites, etc.)

Dynamic API Integration with TMDB API

State Management with useState, useEffect, and Context API

Routing using react-router-dom

Responsive Styling with CSS

Persistent Favorites stored in localStorage

🛠️ Core React Concepts
1. Components

Modular, reusable pieces of UI (e.g., Navbar, MovieCard, Favorites).

Function-based, returning JSX.

Can nest other components.

2. JSX (JavaScript XML)

Hybrid of JavaScript + HTML.

Must return a single parent element.

Supports dynamic expressions via {}.

Uses className instead of class.

3. Props

Allow parent → child data transfer.

Example: <MovieCard movie={movie} />.

4. State Management

useState for local state (e.g., search input, movie results).

useContext for global state (favorites list).

Persistence via localStorage.

5. Side Effects (useEffect)

Used for API calls and localStorage sync.

Runs on initial render ([]) or when dependencies change.

6. Conditional Rendering

Show different UI states using:

Ternary (condition ? A : B)

Logical AND (condition && A).

7. Routing

Implemented with react-router-dom.

Supports:

/ → Home (popular movies)

/favorites → Saved movies

Uses <BrowserRouter>, <Routes>, <Route>, and <Link>.

🌐 API Integration

This project uses The Movie Database (TMDB) API to fetch movies.

Popular Movies: GET /movie/popular

Search Movies: GET /search/movie?query=...

Requires an API Key from TMDB.

Service Layer (services/api.js)

getPopularMovies() → Fetches trending movies.

searchMovies(query) → Fetches search results.

Best Practices

Async/await for API calls.

try...catch for error handling.

loading + error state management.

Centralized service file for API logic.🧑‍💻 State Management
Local State (useState)
const [searchQuery, setSearchQuery] = useState('');
const [movies, setMovies] = useState([]);

Global State (Context API)

MovieProvider wraps app and shares favorites across components.

useContext lets any component access favorites.

Persistence (localStorage)

Saves favorites even after refresh:

localStorage.setItem("favorites", JSON.stringify(favorites));

🏗️ Component-Based Architecture

App.jsx → Root, handles routing.

Navbar.jsx → Navigation with <Link>.

MovieCard.jsx → Displays individual movie details.

Favorites.jsx → Lists saved movies.

Search.jsx → Search input & API calls.

Context/MovieContext.jsx → Global state (favorites).

📍 Page Routing (react-router-dom)

Setup:

npm install react-router-dom


Usage:

import { BrowserRouter, Routes, Route } from "react-router-dom";

<BrowserRouter>
  <Routes>
    <Route path="/" element={<Home />} />
    <Route path="/favorites" element={<Favorites />} />
  </Routes>
</BrowserRouter>


Navigation with <Link to="/favorites">Favorites</Link>.

⚡ Getting Started
1. Prerequisites

Node.js
 installed

Code editor (VS Code recommended)

2. Installation
# Clone the repo
git clone https://github.com/<your-username>/<your-repo>.git

# Navigate to project
cd <your-repo>

# Install dependencies
npm install

3. Run the App
npm run dev


Your app will be running at http://localhost:5173/.

📂 Project Structure
src/
 ┣ components/
 ┃ ┣ Navbar.jsx
 ┃ ┣ MovieCard.jsx
 ┣ pages/
 ┃ ┣ Home.jsx
 ┃ ┣ Favorites.jsx
 ┣ context/
 ┃ ┣ MovieContext.jsx
 ┣ services/
 ┃ ┣ api.js
 ┣ App.jsx
 ┣ main.jsx

🎨 Styling

Modular CSS files imported per component.

Clean, reusable style structure.

📖 Learn More

React Documentation

React Router

TMDB API Docs

📌 Summary

This project demonstrates:

React fundamentals (components, props, state, hooks)

API integration

Component-based architecture

Routing with react-router-dom

Persistent state with localStorage

A great starting point for anyone learning React + APIs + routing.
