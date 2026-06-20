CONVERGENCE — Five-Track Tech & Ideas Summit
Event website — offline-ready static site
==============================================

WHAT'S INSIDE
  index.html          Landing page — overview of all 5 tracks
  startup.html        Track 01 — Startup & Entrepreneurship
  history.html        Track 02 — Technology History & Future Trends
  research.html       Track 03 — Research & Academic Exploration
  cybersecurity.html  Track 04 — Cybersecurity & Threat Intelligence
  business.html       Track 05 — Business & Market Analysis
  assets/style.css    Shared design system (colors, type, layout)

HOW TO RUN IT ON THE DAY OF THE EVENT

Easiest option — just open it:
  Double-click index.html. It opens in your default browser and works
  completely offline. All navigation between tracks works as local files.

Better option — run a tiny local server (recommended if projecting
on a shared screen or letting attendees scan a QR code on the same wifi):

  1. Open a terminal in this folder.
  2. Run:
       python3 -m http.server 8000
     (Windows: "python -m http.server 8000")
  3. On the SAME laptop, visit:  http://localhost:8000
  4. If attendees are on the same wifi network, find your laptop's
     local IP address (e.g. 192.168.1.42) and share:
       http://192.168.1.42:8000
     so they can browse the site on their own phones.

NOTE ON FONTS
  The site loads its display fonts (Fraunces, Inter, JetBrains Mono)
  from Google Fonts over the internet. With no internet connection,
  it will automatically fall back to clean system fonts — the layout
  and design system still work fine, just with a slightly different
  typeface. For a fully offline guarantee with the exact fonts,
  download the three font families and update the @import line at
  the top of assets/style.css to point to local font files instead.

EDITING CONTENT
  Each track page is self-contained HTML — open it in any text editor
  and edit the text directly (session titles, dates, room numbers,
  RSVP links, etc.). The shared visual styling lives in assets/style.css,
  so changes there apply to every page at once.
