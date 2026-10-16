# LocalKart

A mobile-first local marketplace MVP built with HTML, CSS and vanilla JavaScript. It is designed for GitHub Pages and requires no server, build step, API key or third-party JavaScript library.

## Run locally

1. Download or clone this folder.
2. Open `index.html` in a modern browser. Most marketplace features work directly from the file system.
3. For PWA installation and service-worker offline caching, serve the folder over HTTPS or localhost. GitHub Pages provides HTTPS.

## Demo accounts

- Customer: `customer@localkart.demo` / `123456`
- Seller: `seller@localkart.demo` / `123456`

Select Profile to sign in. The demo seller manages Green Basket Grocery. Seed data contains 8 shops, 40 products, 10 categories and 2 sample orders.

## Deploy to GitHub Pages

1. Create a GitHub repository named `localkart` (or any name you prefer).
2. Upload all files and folders from this project; keep the directory structure intact and make `index.html` the repository-root entry point.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**, choose `main` and `/(root)`, then save.
5. Open the published Pages URL. If you change files later, commit and push the changes.

If the project is kept inside a subfolder in your repository, move its contents to the repository root or configure Pages to publish the folder that contains `index.html`.

## Features

- Search across shops and products, category browsing, price/rating/distance/stock filters and sorting.
- Shop and product detail views, recently viewed products, cart quantities and one-shop-at-a-time demo checkout.
- Order IDs, order history, delivery address, COD and a clearly marked UPI placeholder.
- Demo customer profile, saved addresses, light/dark theme, manually entered location and optional browser geolocation.
- Seller overview, product create/edit/delete, stock and price management, shop profile settings, incoming orders and order-status changes.
- WhatsApp contact links for shops with stored phone numbers.
- PWA manifest and service worker for previously cached static files.

## Storage and important limitations

The browser stores the sample catalogue, user session, cart, orders and shop settings in LocalStorage. Data is local to that browser/device and is not shared with another customer or seller device. This is a prototype, not a secure multi-user marketplace. Anyone with browser access can inspect or modify LocalStorage; the demo password is intentionally not secure. Never use this authentication or storage model for real customer accounts, payment details or sensitive information.

UPI is only a placeholder; there is no payment processing. Geolocation only saves a coarse coordinate label and does not calculate real distances. Demo shop distances and ratings are sample data. Checkout currently supports products from one shop per order. Product images can be an emoji or a direct HTTPS image URL; no image upload server is included.

## Backend-ready functions

Storage and business logic are kept in functions such as `getProducts()`, `getShops()`, `getOrders()`, `createOrder()`, `updateOrder()`, `loginUser()` and `saveProduct()`. Replace the LocalStorage access layer with Firebase, Supabase, Appwrite or a custom API when adding secure multi-device accounts, stock synchronisation, real notifications and payments. Production authentication and authorization must be enforced server-side.
