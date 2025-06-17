# 🎬 react-usepopcorn

A lightweight React hook & demonstration app for fetching and displaying movie data using the [OMDb API](http://www.omdbapi.com/). Features include searching, listing results, and showing movie details like posters, ratings, and descriptions.

## 🚀 Features

- Real-time movie search with instant results  
- Show movie poster, title, release year, runtime, genres, plot, and ratings  
- Designed as a reusable `usePopcorn` React hook  
- Simple, clean UI with responsive design  

---

## ⚙️ Setup & Usage

### 1. Clone the Repo


git clone https://github.com/Sudarshanhingalje/react-usepopcorn.git

cd react-usepopcorn

2. Install Dependencies
   
bash
npm install

4. Get OMDb API Key
Register at OMDb API and get your free API key.

5. Create .env File

REACT_APP_OMDB_KEY=your_api_key_here
6. Run Locally

npm start
Open http://localhost:3000 to view the app.

📦 usePopcorn Hook
Use it like this:


import { usePopcorn } from "./hooks/usePopcorn";

function App() {
  const { movies, error } = usePopcorn(searchQuery);

  return movies.map(movie => (
    <div key={movie.imdbID}>
      <img src={movie.Poster} alt={movie.Title} />
      <h3>{movie.Title}</h3>
      <p>{movie.Year}</p>
      {/* ... */}
    </div>
  ));
}
The hook manages fetching, error handling, and state, returning JSON data from the OMDb API.


🔧 Future Enhancements
Add loading spinner and pagination

Filter by genre, year, or rating

Add favorites list with localStorage

Use React Router for a detail page

🙋‍♂️ Author
Sudarshan Hingalje
📱 Instagram – @vanguard.ace
🔗 LinkedIn – sudarshanhingalje

Made with ❤️ and Popcorn 🍿.
Enjoy building and customizing!
