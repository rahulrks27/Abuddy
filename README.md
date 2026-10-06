# Abuddy · Universal Off-Campus Student Accommodation Platform

Abuddy helps students discover, compare, shortlist, and book visits for verified off-campus accommodations, hostels, and PGs near college campuses.

---

## 🚀 Live Multi-Device Presentation Guide

This web application is built for live audience demonstrations across two devices:

### Step 1: Presentation Setup
1. **On the Presentation Laptop**:
   - Open your deployed URL: `https://abuddy-hospitality.vercel.app` (or test locally).
   - Keep the laptop screen visible to the audience in **Student** or **Guest** view.
   - You will see the green **Live Sync** badge in the header, confirming real-time cloud connectivity.

2. **On Your Mobile Phone**:
   - Open the same URL on your phone's browser (Safari or Chrome).
   - Sign in as **Landlord** (e.g. via Google Sign-In or email).
   - Tap **Add property** in the navigation bar.

### Step 2: The Live Demonstration Flow
1. **Fill Property Details on Phone**:
   - Type a title (e.g., *Deluxe Balcony Room · Near College Gate*).
   - Type locality/address (e.g., *Green Valley Colony*).
   - Select room type (e.g., *Single*, *Double Sharing*, or *Custom Sharing*).
   - Set rent and amenities.
   - Attach photos from your phone camera or gallery.
2. **Hit "Publish listing" on your Phone**:
   - In less than 100 milliseconds across the internet:
     - The **Presentation Laptop** plays a notification chime.
     - A live corner pop-up animates: *"Just Listed: [Title] by [Your Name] · Green Valley Colony"*.
     - The stay appears immediately at the very top of the student browse grid.
     - Clicking *"View details ₒ"* on the laptop displays the exact details and photos uploaded from your phone.

---

## 🌗 1-Click Deployment to Vercel via GitHub

1. **Push this folder to GitHub**:
   - Create a new repository on [GitHub](https://github.com/new) named `abuddy`.
   - Upload or push these files:
     - `index.html` (Main web application)
     - `vercel.json` (Vercel routing & security headers)
     - `favicon.png` (Abuddy icon)
     - `schema.sql` (Supabase cloud schema)
     - `README.md` (Project guide)
2. **Deploy on Vercel**:
   - Go to [Vercel](https://vercel.com/new).
   - Import your GitHub repository.
   - Set Framework Preset to *Other* (Root directory: `./`).
   - Click *Deploy*.
   - Your site is live at `your-project.vercel.app`!

---

## ⚡ Supabase PostgreSQL Cloud Database Integration

Abuddy comes pre-wired for Supabase with zero backend coding required. Follow these 4 simple steps to connect your Supabase database:

### 1. Create a Free Supabase Project
- Sign up or log in at [supabase.com](https://supabase.com).
- Click **"New project"**.
- Name: `abuddy` (set a secure database password).
- Region: Select the region nearest to you (e.g. `South Asia (Mumbai)`).
- Click **"Create new project"** (takes ~1 minute to provision).

### 2. Run the Database Schema
- In your Supabase dashboard, click **"SQL Editor"** on the left menu.
- Click **"New query"**.
- Copy and paste the entire content of [`schema.sql`](./schema.sql).
- Click **"Run"** (green button).
- You will see `"Success. No rows returned"`. Tables `stays` and `visit_requests` are now created with Row-Level Security and Realtime Replication enabled.

### 3. Retrieve Your Project API Credentials
- In Supabase, go to **Project Settings** (gear icon at the bottom left) $\rightarrow$ **API**.
- Under **Project URL**, copy the `URL` (e.g., `https://xyzcompany.supabase.co`).
- Under **Project API keys**, copy the `anon` `public` key (e.g., `eyJhbGciOi...`).

### 4. Connect Abuddy
Choose either method:
- **Method A (Direct in Code - Recommended for Vercel)**:
  Open `index.html` and fill lines 1541-1542:
  ```javascript
  window.ABUDDY_SUPABASE_URL = "https://xyzcompany.supabase.co";
  window.ABUDDY_SUPABASE_KEY = "eyJhbGciOi...";
  ```
  Every device visiting your website will now automatically connect to your database without any manual steps!
- **Method B (Live UI Modal)**:
  On your website, click the green **"Live Sync"** badge in the top navigation bar, paste your **Supabase Project URL** and **Anon Key**, and click **"Save & Connect"**.
