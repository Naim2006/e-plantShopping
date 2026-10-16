# Paradise Nursery Shopping Application

A modern and responsive shopping cart web application for **Paradise Nursery**, an online plant store offering a diverse variety of houseplants to create greener, healthier homes and workspaces.

---

## 🌿 Project Overview

Paradise Nursery is built as part of the **IBM / Coursera: Developing Front-End Apps with React** final project. The application demonstrates component-based architecture, dynamic data rendering, event handling, and global state management using **React** and **Redux Toolkit**.

---

## ✨ Features

- **Landing Page:**
  - Company branding ("Paradise Nursery - Where Green Meets Serenity")
  - Engaging background imagery and company mission overview (`AboutUs.jsx`)
  - "Get Started" button smoothly navigating to the plant catalog

- **Navigation Bar:**
  - Brand header linking back to the landing page
  - Direct navigation links to "Plants" catalog and "Cart"
  - Dynamic shopping cart badge displaying the total count of items in real-time

- **Product Catalog (`ProductList.jsx`):**
  - Displays distinct plant categories:
    - *Air Purifying Plants*
    - *Aromatic Fragrant Plants*
    - *Insect Repellent Plants*
    - *Medicinal Plants*
    - *Low Maintenance Plants*
  - Detailed plant cards showing thumbnail image, plant name, description, unit price, and an "Add to Cart" action button.
  - Buttons update state to "Added to Cart" and disable once added to prevent accidental duplicate actions.

- **Shopping Cart (`CartItem.jsx`):**
  - Lists all selected plants with thumbnail, plant name, unit cost, quantity, and item subtotal.
  - Interactive `+` and `-` quantity adjustment buttons.
  - Individual item deletion (`Delete` button).
  - Real-time calculation and display of the total cart amount.
  - "Continue Shopping" button returning users back to the product list.
  - "Checkout" button with coming-soon confirmation.

- **State Management (`CartSlice.jsx` & `store.js`):**
  - Powered by **Redux Toolkit** (`createSlice`, `configureStore`, `useDispatch`, `useSelector`).
  - Reducers: `addItem`, `removeItem`, `updateQuantity`.

---

## 🛠️ Tech Stack

- **Frontend Library:** React 18
- **State Management:** Redux Toolkit (`@reduxjs/toolkit`), `react-redux`
- **Build Tool:** Vite
- **Styling:** CSS3 (Flexbox, Media Queries for responsive layout)
- **Deployment:** GitHub Pages / Static Hosting

---

## 📁 Project Structure

```text
e-plantShopping/
├── public/
│   └── vite.svg
├── src/
│   ├── assets/
│   │   └── react.svg
│   ├── AboutUs.css
│   ├── AboutUs.jsx          # Company mission and background info
│   ├── App.css              # Main application styling and transitions
│   ├── App.jsx              # Root component managing view toggling
│   ├── CartItem.css         # Shopping cart styling
│   ├── CartItem.jsx         # Cart items list, subtotals, and quantity controls
│   ├── CartSlice.jsx        # Redux Toolkit slice for shopping cart state
│   ├── index.css            # Base stylesheet
│   ├── main.jsx             # React DOM root setup with Redux Provider
│   ├── ProductList.css      # Catalog layout and responsive grid styles
│   ├── ProductList.jsx      # Plant listing grouped by categories with Add to Cart
│   └── store.js             # Redux store configuration
├── index.html
├── package.json
├── vite.config.js
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js (v18 or higher recommended)
- npm (Node Package Manager)

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/e-plantShopping.git
   cd e-plantShopping
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the local development server:
   ```bash
   npm run dev
   ```

4. Open your browser and navigate to the local address (e.g., `http://localhost:5173`).

---

## 📦 Building for Production

To create an optimized production build:
```bash
npm run build
```

To preview the production build locally:
```bash
npm run preview
```

---

## 🌐 Deployment to GitHub Pages

1. Ensure the `base` property in `vite.config.js` is set to your repository name:
   ```javascript
   export default defineConfig({
     base: '/e-plantShopping/',
     plugins: [react()],
   })
   ```

2. Deploy using `gh-pages`:
   ```bash
   npm run deploy
   ```

---

## 📄 License

This project was developed for educational purposes as part of the IBM Front-End Developer Professional Certificate program.