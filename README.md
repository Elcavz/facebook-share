================================================================================
                           ELCAVZFLIXTER - MOVIE SHARE HUB
================================================================================

A web application that allows users to discover movies, watch trailers, and share
movie information with viral hashtags directly to Facebook.

================================================================================
                           LIVE DEMO
================================================================================

Website: https://www.elcavzflixter.site

================================================================================
                           FEATURES
================================================================================

✓ Search movies by title (powered by TMDB API)
✓ Browse trending and now playing movies
✓ Watch official YouTube trailers (embedded player)
✓ Generate viral hashtags automatically for each movie
✓ Copy complete movie info + trailer link + hashtags to clipboard
✓ Share to Facebook with auto-filled movie details and hashtags
✓ Mark movies as "Shared" (saved in browser localStorage)
✓ Track total shared movies count
✓ Mobile responsive design
✓ No Facebook CSP errors (plain text sharing)

================================================================================
                           TECH STACK
================================================================================

Frontend: HTML5, CSS3, JavaScript (Vanilla)
API: TMDB (The Movie Database) API v3
Icons: Font Awesome 6
Storage: LocalStorage (for shared movies tracking)

================================================================================
                           API KEY USED
================================================================================

TMDB API Key: b25412885fcb808bb37e93b4c6ccb763

Note: This key is embedded in the code for demo purposes.
For production, please use environment variables or backend proxy.

================================================================================
                           HOW TO USE
================================================================================

1. Open the website in any modern browser
2. Browse trending movies or search for any movie
3. Click on a movie card to:
   - Watch the official trailer
   - View full movie synopsis, rating, and release year
4. Choose action:
   - [Share on Facebook] - Opens Facebook share dialog with auto-filled content
   - [Copy Viral Post] - Copies movie info + trailer link + hashtags
   - [Mark as Shared] - Tracks that you've shared this movie
5. Shared movies are highlighted with a gold border and "Shared" badge

================================================================================
                           FACEBOOK SHARE FORMAT
================================================================================

When you click "Share on Facebook", the following content is auto-filled:

🔥✨ "Movie Title" (Year) - Must Watch!

📖 SYNOPSIS: Movie description text...

⭐ 8.5/10

▶️ OFFICIAL TRAILER: https://youtube.com/watch?v=xxxxx

🎬 WATCH THE FULL MOVIE: https://www.elcavzflixter.site

#ElcavzFlixter #NowWatching #MovieViral #TrailerDrop #CinemaLovers
#MovieTitle #MustWatchMovie #StreamIt #FilmCommunity

👥 Tag a friend who needs to see this! #TrendingNow #MovieNight

================================================================================
                           HASHTAGS GENERATED
================================================================================

Each movie automatically gets these trending hashtags:

- #ElcavzFlixter (your brand)
- #NowWatching
- #MovieViral
- #TrailerDrop
- #CinemaLovers
- #[MovieTitleWithoutSpaces]
- #MustWatchMovie
- #StreamIt
- #FilmCommunity

================================================================================
                           PROJECT STRUCTURE
================================================================================

index.html          - Main application file (HTML, CSS, JavaScript)
readme.txt          - This documentation file

All code is contained in a single HTML file for easy deployment.

================================================================================
                           CUSTOMIZATION
================================================================================

Change Website URL:
Search for "MY_WEBSITE" constant and update the URL.

Change API Key:
Search for "API_KEY" constant and replace with your TMDB API key.

Change Hashtags:
Modify the "baseHashtags" array in generateTrendingHashtags() function.

Change Shared Movies Storage Key:
Search for "elcavz_shared_movies" in localStorage functions.

================================================================================
                           BROWSER SUPPORT
================================================================================

✓ Chrome (latest)
✓ Firefox (latest)
✓ Safari (latest)
✓ Edge (latest)
✓ Mobile browsers (iOS/Android)

================================================================================
                           KNOWN ISSUES
================================================================================

None. The Facebook share functionality uses plain text sharing to avoid
CSP (Content Security Policy) errors that occur when embedding videos.

================================================================================
                           DEPLOYMENT
================================================================================

Simply upload the index.html file to any web server or hosting service.

Recommended: GitHub Pages, Netlify, Vercel, or any static hosting.

================================================================================
                           FILES INCLUDED
================================================================================

1. index.html - Complete web application
2. readme.txt - Documentation (this file)

================================================================================
                           CREDITS
================================================================================

Movie Data: The Movie Database (TMDB) - https://www.themoviedb.org
Icons: Font Awesome - https://fontawesome.com
Font: Inter - Google Fonts

Developed by: Renz Bautista Sayaman

================================================================================
                           LICENSE
================================================================================

This project is for educational and demonstration purposes.
TMDB API usage requires attribution to TMDB.

================================================================================
                           CONTACT
================================================================================

Website: https://www.elcavzflixter.site

================================================================================
                           VERSION HISTORY
================================================================================

v1.0 - Initial release
  - Movie search and trending
  - YouTube trailer embedding
  - Facebook share with auto-filled content
  - Viral hashtags generation
  - Shared movies tracking
  - Copy to clipboard functionality

================================================================================
                           END OF README
================================================================================
