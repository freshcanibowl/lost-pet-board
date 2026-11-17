# Lost Pet Board 🐾

A warm, mobile-first single-page app for posting and finding lost & found pets in Malaysia. Posts are stored in **Supabase** (free PostgreSQL backend), so everyone sees the same shared board.

**Live site:** https://freshcanibowl.github.io/lost-pet-board/

## Features

- **Post a pet** — lost/found toggle, pet type, name, area, short note, contact, emoji photo sticker
- **Active posts** — everyone's current posts, newest first
- **Returned pets** — mark a pet as returned and it moves to the happy-endings list
- No login required — posts are public (protected by row-level security)

## Setup (one-time, ~5 minutes)

1. Create a free project at [supabase.com](https://supabase.com)
2. Open **SQL Editor** in the Supabase dashboard, paste the contents of [`schema.sql`](schema.sql), and run it
3. In Supabase go to **Settings → API**, copy the **Project URL** and **anon public key**
4. Open `index.html` and paste them into the config block near the bottom:

   ```js
   const SUPABASE_URL = 'https://YOUR-PROJECT.supabase.co';
   const SUPABASE_ANON_KEY = 'YOUR-ANON-KEY';
   ```

5. Commit and push — the live GitHub Pages site will update automatically

Until step 4 is done, the site shows a friendly banner saying Supabase isn't configured yet.

## Running locally

Just open `index.html` in a browser — no build step or server needed.

## Tech

- Plain HTML/CSS/JS (single file, no build tooling)
- Supabase JS v2 via CDN
- GitHub Pages hosting
