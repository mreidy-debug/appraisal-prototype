Appraisal Workspace v6 - static prototype

Host this whole folder as-is on any static web server (S3, Netlify, GitHub Pages, internal web server, etc.).
Keep the folder structure; the page loads files by relative path.

  index.html                         -> redirects to the prototype
  Appraisal Workspace v6.dc.html     -> the prototype page
  Customer Offer Sheet.dc.html       -> consumer-facing offer sheet (opened by "View customer offer")
  support.js, image-slot.js          -> page runtime
  _ds/                               -> CarGurus design system CSS, fonts, bundle
  assets/                            -> vehicle photos, window sticker, CARFAX image

Notes
- It must be served over http(s); opening the file directly from disk (file://) will not work.
- The runtime loads React 18.3.1 and Babel 7.29.0 from unpkg.com, so viewers need internet access to unpkg.com.
- All data is sample/mock data. The Customize layout choice is saved in each viewer's browser.
- Quick local test: run "python3 -m http.server 8000" in this folder, then open http://localhost:8000/
