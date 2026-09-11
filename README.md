# Lumina Workspace - Modern Business Website

A premium, modern, fully functional business website built strictly with HTML5, CSS3 (Tailwind CSS v4), and Vanilla JavaScript. 

## Features

- **Multi-page Architecture**: Home, About Us, Product Information, and Contact pages.
- **Modern Design**: Clean layout, generous whitespace, strong visual hierarchy.
- **Vanilla JavaScript**: Lightweight interactions without relying on heavy frameworks like React or Vue.
- **Responsive**: Fully optimized for mobile, tablet, and desktop screens (320px to 1920px).
- **Interactive Elements**: 
  - Smooth scroll reveals
  - Responsive mobile navigation
  - FAQ accordion
  - Testimonials carousel
  - Image gallery lightbox
  - Form validation UI
- **Performance Optimized**: Zero bloat, fast loading.

## Technologies Used

- HTML5
- CSS3 (Tailwind CSS v4 via Vite)
- Vanilla JavaScript
- Lucide Icons (SVG)
- Vite (Build Tooling)

## Local Development Setup

To run this project locally:

1. Ensure you have Node.js installed.
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the Vite development server:
   ```bash
   npm run dev
   ```

## Replacing Content and Images

- **Text Content**: Open the respective HTML files (`index.html`, `about.html`, `product.html`, `contact.html`) and replace the text within the tags.
- **Images**: Search for `img` tags. They currently use `images.unsplash.com` and `pravatar.cc` placeholders. Replace the `src` attributes with your optimized local assets (e.g., `/images/products/my-image.webp`) or own CDN links.

## Formspree Contact Form Integration

To make the contact form fully functional without a custom backend:

1. Sign up for a free account at [Formspree.io](https://formspree.io/).
2. Create a new form in the Formspree dashboard.
3. You will receive an endpoint URL (e.g., `https://formspree.io/f/YOUR_FORM_ID`).
4. Open `contact.html`.
5. Find the form tag: `<form id="contact-form" class="space-y-6" action="#" method="POST">`
6. Replace `action="#"` with `action="https://formspree.io/f/YOUR_FORM_ID"`.
7. You may want to remove the JS override in `script.js` (around line 63) that prevents the default form submission for the mockup success message, allowing Formspree to handle the redirect/submission naturally, or configure AJAX submission via JS.

## Deployment

This website compiles down to static HTML, CSS, and JS, making it perfectly suited for Netlify, GitHub Pages, Vercel, or any standard shared hosting.

### Deploying to Netlify (Recommended)

1. Run the build command to generate the optimized static files:
   ```bash
   npm run build
   ```
2. The built files will be output to the `dist/` directory.
3. Drag and drop the `dist/` folder into the Netlify manual deploy zone, or connect your GitHub repository to Netlify and set the build command to `npm run build` and publish directory to `dist`.

### Deploying to Shared Hosting

1. Run `npm run build`.
2. Upload the contents of the `dist/` folder to your shared hosting environment (usually the `public_html` or `www` directory) via FTP or a web file manager.
