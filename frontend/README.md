# MovieApp

A modern, responsive movie discovery web application built with React and Vite. Search for movies using The Movie Database (TMDB) API, view trending movies based on user searches, and enjoy a sleek UI with Tailwind CSS.

## Features

- **Movie Search**: Search for movies by title with real-time results from TMDB API
- **Trending Movies**: Display top 5 trending movies based on search popularity stored in Appwrite database
- **Debounced Search**: Optimized search with 500ms debounce to reduce API calls
- **Responsive Design**: Mobile-first design that works seamlessly across devices
- **Movie Cards**: Detailed movie information including poster, title, rating, language, and release year
- **Search Analytics**: Tracks search counts and updates trending movies dynamically

## Tech Stack

### Frontend
- **React 19**: Modern React with hooks for state management
- **Vite**: Fast build tool and development server
- **Tailwind CSS 4**: Utility-first CSS framework for styling
- **React Use**: Library for debounced search functionality

### Backend & Database
- **Appwrite**: Backend-as-a-Service for database operations
  - Stores search terms and counts
  - Manages trending movies data

### APIs
- **TMDB API**: The Movie Database API for movie data and posters

### Development Tools
- **ESLint**: Code linting and formatting
- **Vite Plugins**: React plugin for fast refresh

## Getting Started

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn
- Appwrite account and project
- TMDB API key

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd MovieApp/frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory and add your environment variables:
   ```env
   VITE_TMDB_API_KEY=your_tmdb_api_key_here
   VITE_APPWRITE_PROJECT_ID=your_appwrite_project_id
   VITE_APPWRITE_DATABASE_ID=your_appwrite_database_id
   VITE_APPWRITE_COLLECTION_ID=your_appwrite_collection_id
   ```

4. Start the development server:
   ```bash
   npm run dev
   ```

5. Open [http://localhost:5173](http://localhost:5173) in your browser.

### Build for Production

```bash
npm run build
```

### Preview Production Build

```bash
npm run preview
```

## Project Structure

```
frontend/
├── public/
│   └── vite.svg
├── src/
│   ├── assets/
│   │   ├── hero-bg.png
│   │   ├── hero.png
│   │   ├── logo.png
│   │   ├── no-movie.png
│   │   ├── search.svg
│   │   └── star.svg
│   ├── components/
│   │   ├── MovieCard.jsx
│   │   ├── Search.jsx
│   │   └── Spinner.jsx
│   ├── App.css
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
├── appwrite.js
├── package.json
├── vite.config.js
└── README.md
```

## Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `VITE_TMDB_API_KEY` | Your TMDB API key | Yes |
| `VITE_APPWRITE_PROJECT_ID` | Appwrite project ID | Yes |
| `VITE_APPWRITE_DATABASE_ID` | Appwrite database ID | Yes |
| `VITE_APPWRITE_COLLECTION_ID` | Appwrite collection ID for search data | Yes |

## API Usage

The app uses TMDB API endpoints:
- `/search/movie`: For movie search
- `/discover/movie`: For popular movies (fallback)

Appwrite is used for:
- Storing search terms and counts
- Retrieving trending movies

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run linting: `npm run lint`
5. Submit a pull request

## License

This project is licensed under the MIT License.
