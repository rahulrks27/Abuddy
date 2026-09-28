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
     - `google-auth.html` (Interactive Google OAuth popup)
     - `vercel.json` (Vercel routing & caching headers)
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

## 🐑 Supabase PostgreSQL Cloud Database (Included & Ready)

The application works 100% out of the box with zero configuration using the built-in real-time cloud relay. If you also wish to persist all data to your Supabase PostgreSQL database:

1. Create a project at [Supabase](https://app.supabase.com).
2. Go to the **SQL Editor** and run the script in `schema.sql`.
3. In the Abuddy web header, click the **Live Sync** badge and paste your **Supabase URL** and **Anon Key**.
4. Click **Save & Connect**. Stays will now also persist to your PostgreSQL cloud database!
