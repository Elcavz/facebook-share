# 🎬 ElcavzFlixter — Viral Movie Share + Trailer Hub

> Discover trending movies, watch trailers, and share viral posts — all in one cinematic experience.

![ElcavzFlixter](https://www.elcavzflixter.site/og-image.jpg)

---

## 🍿 Live Site

**[https://www.elcavzflixter.site](https://www.elcavzflixter.site)**

---

## 📖 Overview

ElcavzFlixter is a single-page web application that lets users browse now-playing and trending movies, watch official trailers, and generate ready-to-paste viral social media posts — complete with trending hashtags. It's built with vanilla HTML, CSS, and JavaScript, powered by the [TMDB API](https://www.themoviedb.org/documentation/api).

---

## ✨ Features

- **🔥 Trending & Now Playing** — Loads up to 50 currently trending/now-playing movies on launch
- **🔍 Movie Search** — Search any movie by keyword using TMDB's search endpoint
- **▶️ Trailer Playback** — Watch official YouTube trailers embedded directly in a modal
- **📋 Viral Post Generator** — Auto-generates a shareable post with synopsis, rating, trailer link, website link, and trending hashtags
- **📘 Facebook Share** — One-click Facebook share button (opens Facebook sharer with your site as the link)
- **✅ Shared Tracker** — Marks movies as shared, persists across sessions via `localStorage`, and visually highlights shared cards
- **#️⃣ Hashtag Engine** — Dynamically generates movie-specific and evergreen hashtags for maximum reach
- **📱 Responsive Design** — Mobile-friendly layout with adaptive grid

---

## 🖥️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML5, CSS3, Vanilla JavaScript (ES2020+) |
| Movie Data | [TMDB API v3](https://developers.themoviedb.org/3) |
| Trailers | YouTube Embed via TMDB video endpoint |
| Icons | [Font Awesome 6](https://fontawesome.com/) |
| Storage | Browser `localStorage` |
| Sharing | Facebook Sharer API |

---

## 🚀 Getting Started

No build tools or package manager required. This is a pure static site.

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/elcavzflixter.git
cd elcavzflixter
```

### 2. Open in a browser

Simply open `index.html` in your browser:

```bash
open index.html
# or on Windows:
start index.html
```

Or serve it locally with any static server:

```bash
npx serve .
# or
python3 -m http.server 8080
```

### 3. Configure your API Key

In `index.html`, locate the configuration block near the top of the `<script>` tag and replace the values:

```js
const API_KEY = 'YOUR_TMDB_API_KEY';   // Get one free at https://www.themoviedb.org/settings/api
const MY_WEBSITE = 'https://your-site-url.com';
```

> ⚠️ **Never commit your API key to a public repository.** Consider using environment variables or a backend proxy for production.

---

## 🔑 Getting a TMDB API Key

1. Create a free account at [themoviedb.org](https://www.themoviedb.org/)
2. Go to **Settings → API**
3. Request an API key (v3 auth)
4. Copy the key and paste it into the config block in `index.html`

---

## 📁 Project Structure

```
elcavzflixter/
│
├── index.html          # Main (and only) application file
│                       # Contains all HTML, CSS, and JavaScript
└── README.md           # This file
```

> The entire app lives in a single `index.html` file — no frameworks, no bundlers, no dependencies to install.

---

## 🎯 How It Works

### Movie Loading
On page load, the app calls TMDB's `/movie/now_playing` endpoint. If no results are returned, it falls back to `/movie/popular`. Up to 50 movies are displayed in a responsive card grid.

### Search
Searches hit TMDB's `/search/movie` endpoint in real time when the user clicks **Find Movie** or presses `Enter`.

### Trailer Modal
Clicking any movie card (or the **Trailer** button) fetches the movie's video list from TMDB and picks the first official YouTube trailer. It renders as an embedded `<iframe>` inside a full-screen modal.

### Viral Post Generation
The `generateViralCopyText()` function assembles a shareable text post including:
- Movie title and release year
- Synopsis (truncated to ~250 chars for Facebook)
- Star rating and vote count
- YouTube trailer link
- Link to `MY_WEBSITE`
- Dynamically generated hashtags

### Shared Movie Tracking
Clicking **✅ Mark as Shared** saves the movie ID to `localStorage`. Shared movies get a gold border and badge across sessions.

---

## 🔧 Configuration Reference

| Variable | Description | Default |
|---|---|---|
| `API_KEY` | Your TMDB API v3 key | `b25412885f...` *(replace this)* |
| `BASE_API` | TMDB base API URL | `https://api.themoviedb.org/3` |
| `IMG_BASE` | TMDB image CDN base | `https://image.tmdb.org/t/p/w500` |
| `MY_WEBSITE` | Your site URL appended to all share posts | `https://www.elcavzflixter.site` |
| `FALLBACK_POSTER` | Placeholder image when no poster exists | `via.placeholder.com` |

---

## 📲 Sharing Flow

```
User clicks Share / Copy
        │
        ├─ Facebook Share → Opens facebook.com/sharer with your site URL
        │
        └─ Copy Viral Post → Copies full text post to clipboard
                              (title, synopsis, rating, trailer link,
                               website link, hashtags, friend tag CTA)
```

---

## 🌐 Open Graph Meta Tags

The app includes OG meta tags for rich link previews when the site URL is shared:

```html
<meta property="og:title" content="ElcavzFlixter - Watch Movies" />
<meta property="og:description" content="Discover the best movies, watch trailers..." />
<meta property="og:image" content="https://www.elcavzflixter.site/og-image.jpg" />
<meta property="og:url" content="https://www.elcavzflixter.site" />
```

> Make sure `og-image.jpg` exists at your site root for the preview image to display on Facebook/Twitter.

---

## 🗺️ Roadmap / Potential Improvements

- [ ] Add pagination or infinite scroll for more movies
- [ ] Twitter/X share button
- [ ] WhatsApp share button
- [ ] Dark/light mode toggle
- [ ] Genre filter tabs
- [ ] Movie watchlist (save movies to watch later)
- [ ] Move API key to a secure backend proxy
- [ ] PWA support (offline mode, installable)

---

## ⚠️ Disclaimer

This project uses the [TMDB API](https://www.themoviedb.org/) but is not endorsed or certified by TMDB. All movie data, posters, and metadata are property of their respective owners. This app is for personal/educational use only.

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

## 🙌 Credits

- Movie data: [The Movie Database (TMDB)](https://www.themoviedb.org/)
- Icons: [Font Awesome](https://fontawesome.com/)
- Trailers: [YouTube](https://youtube.com/)
