# Job Portal - Vue 3 + Tailwind CSS

A professional job listing website built with Vue 3 (Composition API) and Tailwind CSS.

## Features

- **Responsive Design**: Fully responsive layout for desktop, tablet, and mobile
- **Modern UI**: Clean and professional design matching job portal standards
- **Vue 3 Composition API**: Latest Vue.js features and best practices
- **Tailwind CSS**: Utility-first CSS framework for rapid development
- **Reusable Components**: Modular component architecture
- **Interactive Elements**: Search filters, bookmarks, and hover effects

## Project Structure

```
job-portal-vue/
├── src/
│   ├── components/
│   │   ├── Navbar.vue
│   │   ├── SearchBox.vue
│   │   ├── JobCategories.vue
│   │   ├── CategoryCard.vue
│   │   ├── FeaturedJobs.vue
│   │   ├── JobCard.vue
│   │   ├── JobListingSection.vue
│   │   ├── JobListingCard.vue
│   │   ├── Sidebar.vue
│   │   ├── FeaturedCompanies.vue
│   │   ├── CompanyCard.vue
│   │   └── Footer.vue
│   ├── App.vue
│   ├── main.js
│   └── style.css
├── index.html
├── package.json
├── vite.config.js
├── tailwind.config.js
└── postcss.config.js
```

## Installation & Setup

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn

### Steps

1. **Install Dependencies**

```bash
npm install
```

2. **Run Development Server**

```bash
npm run dev
```

The application will be available at `http://localhost:5173`

3. **Build for Production**

```bash
npm run build
```

4. **Preview Production Build**

```bash
npm run preview
```

## Components Overview

### Navbar
- Logo and branding
- Navigation menu with active states
- Login and Post Job CTA buttons
- Mobile responsive menu

### SearchBox
- Keyword search input
- Location filter
- Category dropdown
- Popular searches tags

### JobCategories
- Grid of category cards
- Icons and job counts
- Hover effects

### FeaturedJobs
- Featured job listings
- Job cards with company info
- Salary, location, and type badges
- Bookmark functionality

### JobListingSection
- Main job listing area
- Detailed job cards
- Tags and descriptions
- Sidebar filters

### Sidebar
- Job type filters
- Salary range options
- Experience level filters
- Apply filters button

### FeaturedCompanies
- Company cards grid
- Company logos and info
- Open positions count

### Footer
- Multi-column layout
- Quick links and resources
- Social media icons
- Copyright information

## Customization

### Colors

Edit `tailwind.config.js` to customize the color scheme:

```javascript
colors: {
  primary: {
    // Your primary colors
  },
  accent: {
    // Your accent colors
  }
}
```

### Content

Update job listings, categories, and company data in respective component files.

## Technologies Used

- **Vue 3**: Progressive JavaScript framework
- **Vite**: Next-generation frontend tooling
- **Tailwind CSS**: Utility-first CSS framework
- **PostCSS**: CSS processing tool
- **JavaScript ES6+**: Modern JavaScript

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

MIT License

## Author

Built with ❤️ using Vue 3 and Tailwind CSS
