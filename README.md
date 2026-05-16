# Nice Gadgets — Product Catalog

An e-commerce product catalog application built with React, TypeScript, and Redux Toolkit. This application allows users to browse smartphones, tablets, and accessories, view detailed product information, manage a shopping cart and a favorites list, and experience advanced UI interactions like theme switching and full-text debounced search.

🌐 **Live Demo:** [https://gtxtab.github.io/phone_cataloge_landing](https://gtxtab.github.io/phone_cataloge_landing)

---

## 🚀 Features

### Core Pages
* **Home Page (`/`):** Includes a dynamic pictures slider (auto-advancing every 5 seconds), "Hot Prices" slider (discounted products), "Brand New Models" slider (newest products by year), and category navigation.
* **Product Catalog Pages (`/phones`, `/tablets`, `/accessories`):** Product lists with dynamic fetching, skeleton loaders, and a custom error state handling.
* **Product Details Page (`/product/:productId`):** Full tech specs, interactive color/capacity selection selectors, a multi-image gallery switcher, and a random "You may also like" suggestion section. Includes interactive Breadcrumbs and a fully functional "Back" button.
* **Shopping Cart Page (`/cart`):** Fully functional cart syncing seamlessly with `localStorage`. Users can modify item quantities, remove items, see real-time price updates, and process a simulated Checkout with confirmation modals.
* **Favorites Page (`/favorites`):** Dedicated area for bookmarked products with badge-counters synchronized globally across the app header.

### Advanced Capabilities & UX
* **🎛️ URL State Synchronization:** Sorting options (`?sort=age|title|price`) and pagination params (`?page=X&perPage=Y`) are stored directly in the URL to preserve view states on page reloads.
* **🔍 Global Search:** Debounced input field integrated dynamically into the header for screens rendering a product list, synced with `?query=value` parameter.
* **🌓 Dark/Light Mode Theme Switcher:** Fully integrated responsive theme layout.
* **✨ Smooth UX:** CSS module transitions on all interactable elements and a strict 10% image scale up animation on card hovers.

---

## 🛠️ Tech Stack & Architecture

* **Frontend Library:** React 18 (Functional components, Hooks, Context API)
* **Language:** TypeScript (Strictly typed schemas for Products and Variants)
* **State Management:** Redux Toolkit (Slices for Cart, Favorites, Global Search)
* **Styling:** SASS (SCSS Modules) with Bulma components integration
* **Testing & Code Quality:** ESLint (Airbnb TypeScript extension), Stylelint, Prettier, Cypress (E2E testing)
* **Build & Deployment:** `mate-scripts` (Webpack wrapper yielding optimized production builds in the `dist/` directory) and `gh-pages`.

### Directory Structure
```text
src/
├── assets/         # Global static images, vectors, and background shapes
├── components/     # Reusable UI elements (iconsSVG, Loader, Footer, Header)
├── context/        # ThemeContext configuration (Dark/Light mode)
├── modules/        # Domain-driven modular pages structure
│   ├── HomePage/
│   ├── CartPage/
│   ├── ProductDetailsPage/
│   └── Shared/     # Shared layout pieces across multi-page systems
├── types/          # Core TypeScript declarations (Product.ts, etc.)
└── utils/          # Utility functions (public path helpers, debounce algorithms)

```

---

## 📦 Installation & Setup

Ensure you have [Node.js](https://nodejs.org/) installed on your computer.

1. **Clone the repository:**
```bash
git clone [https://github.com/gtxtab/phone_cataloge_landing.git](https://github.com/gtxtab/phone_cataloge_landing.git)
cd phone_cataloge_landing

```


2. **Install dependencies:**
Due to rigorous version configurations across custom peer dependencies, use the following command:
```bash
npm install --legacy-peer-deps

```


3. **Run local development server:**
```bash
npm run start

```


Open [http://localhost:3000](https://www.google.com/search?q=http://localhost:3000) in your browser to view the application.

---

## ⚙️ Available Scripts

In the project directory, you can run:

* `npm run start` - Runs the app in development mode with continuous hot-reloading.
* `npm run build` - Compiles and compiles code into an optimized web bundle inside the `dist/` folder.
* `npm run lint` - Sequentially formats and audits your files via Stylelint, Prettier, and ESLint rule trees.
* `npm run test` - Launches the internal testing environments and runs Cypress validation rules.
* `npm run deploy` - Triggers production builds and pushes the updated codebase assets out to GitHub Pages.

---

## 📄 License

This project is open-source software licensed under the **GPL-3.0 License**. Developed as a technical graduation portfolio piece at Mate Academy.

```

```
