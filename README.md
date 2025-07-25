# ✨ Portfolio 

Hi there! 👋
I’m Atik, and this is one of my personal portfolio projects. I built it to showcase my work, skills, and hands-on learning journey in web development.

🎯 Live Demo
[🌐 Website](https://atikaarifiana.vercel.app) 

---

## 🔧 Tech Stack

I used a few modern tools and frameworks to bring this project to life:

* **ReactJS** – for building the frontend components
* **Tailwind CSS** – for clean, utility-first styling
* **Supabase** – as the backend to manage project data, certificates, and comments
* **AOS (Animate On Scroll)** – for smooth scroll animations
* **Framer Motion** – to add some interactive motion
* **Lucide Icons** – clean and elegant icons
* **Material UI** – ready-to-use UI components
* **SweetAlert2** – for custom alert popups 

---

## 📝 Before You Start (Prerequisites)

Make sure you have these installed first:

* **Node.js** v14 or later
* **npm** or **yarn** as your package manager

---

## 🚀 Getting Started

1. **Clone the Repository**

```bash
git clone https://github.com/EkiZR/Portofolio_V5.git
cd Portofolio_V5
```

2. **Install Dependencies**

```bash
npm install
```

If you run into peer dependency issues, try:

```bash
npm install --legacy-peer-deps
```

3. **Run Local Development Server**

```bash
npm run dev
```

4. **Open in Browser**

Typically at:
`http://localhost:5173`

---

## 🏗️ Build for Production

To create an optimized version for deployment:

```bash
npm run build
```

The final files will be available in the `dist` folder.

---

## 🔐 Supabase Configuration

This project uses **Supabase** to store dynamic content like projects, certificates, and user comments.

### 1. Create a Supabase Project

* Go to [Supabase](https://supabase.com/) and sign in
* Copy your Project URL and `anon public key` from **Settings > API**

### 2. Set Up Database & Policies

* Run the provided SQL setup in Supabase’s SQL Editor (can be taken from the original repo)

### 3. Enable Realtime for Comments

* Go to **Database > Replication**
* Enable replication for the `portfolio_comments` table

---

## 🛠️ Environment Setup

Create a `.env` file in your project root and add:

```
VITE_SUPABASE_URL=your-supabase-url
VITE_SUPABASE_ANON_KEY=your-supabase-anon-key
```

Make sure to **exclude `.env` from version control** (never push it to GitHub!)

---

## 📁 Supabase Client Setup (`supabase.js`)

```js
import { createClient } from '@supabase/supabase-js'

const supabaseUrl = import.meta.env.VITE_SUPABASE_URL
const supabaseKey = import.meta.env.VITE_SUPABASE_ANON_KEY

if (!supabaseUrl || !supabaseKey) {
  throw new Error("Supabase URL and Anon Key are required. Please check your .env file.")
}

export const supabase = createClient(supabaseUrl, supabaseKey)
```

---

## 🧩 Troubleshooting

If things don’t work as expected, check the following:

* Is Node.js properly installed?
* Are you in the correct project folder?
* Is your `.env` file properly set up with correct keys?
* Try restarting the dev server after any config changes
* Clear your browser cache if you’re stuck on old assets
---
