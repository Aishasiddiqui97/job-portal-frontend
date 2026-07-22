# 🚀 Quick Start Guide

## Step 1: Install Dependencies

Open your terminal in the project folder and run:

```bash
npm install
```

This will install:
- Vue 3
- Vite
- Tailwind CSS
- All required dependencies

## Step 2: Start Development Server

```bash
npm run dev
```

Your job portal will open at: **http://localhost:5173**

## Step 3: View in Browser

Open your browser and go to the URL shown in the terminal.

## 🎉 That's it! Your job portal is running!

---

## Project Structure

```
job-portal-vue/
├── src/
│   ├── components/        # All Vue components
│   ├── App.vue           # Main app component
│   ├── main.js           # App initialization
│   └── style.css         # Global styles
├── index.html            # HTML entry
├── package.json          # Dependencies
├── tailwind.config.js    # Tailwind config
└── vite.config.js        # Vite config
```

---

## Available Scripts

```bash
npm run dev      # Start development server
npm run build    # Build for production
npm run preview  # Preview production build
```

---

## Features Included

✅ **Navigation Bar** - With logo, menu, and CTA buttons
✅ **Hero Search** - Keyword, location, and category filters
✅ **Job Categories** - 8 popular categories with icons
✅ **Featured Jobs** - Job cards with bookmark feature
✅ **Job Listings** - Detailed listings with sidebar filters
✅ **Companies** - Featured companies section
✅ **Footer** - Complete footer with links and social media

---

## Customize Your Portal

### Change Colors
Edit `tailwind.config.js`:

```javascript
colors: {
  primary: {
    600: '#YOUR_COLOR'
  }
}
```

### Edit Job Data
Edit component files in `src/components/` to change:
- Job listings
- Categories
- Companies
- Any content

### Add More Jobs
Go to `FeaturedJobs.vue` and `JobListingSection.vue` to add more job data.

---

## Tech Stack

- **Vue 3** - Progressive JavaScript framework
- **Tailwind CSS** - Utility-first CSS
- **Vite** - Fast build tool
- **HTML5 & CSS3** - Modern web standards

---

## Need Help?

Check `README.md` for detailed documentation.

Happy coding! 🎉
