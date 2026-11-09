# ABH SPORTS — Built for the Win

**EF101 Project 18: Mini E-Commerce Store for Cricket Products**

A beginner-friendly Node.js + Express e-commerce project with a Miandad Sports-inspired shopping journey and original ABH SPORTS branding. The design uses black, red and white, with a responsive catalogue, product detail views, saved items, variant selectors, order tracking, checkout and admin controls.

## Requirements
- Node.js 18 or newer
- npm (installed with Node.js)
- A modern web browser

## Run on Windows (VS Code)
1. Extract `ABH-SPORTS-Ecommerce-Project.zip` to a folder such as Desktop.
2. Open that extracted folder in VS Code (**File → Open Folder**).
3. Open **Terminal → New Terminal**.
4. Run `npm install` and wait for it to finish.
5. Run `npm start`.
6. Open `http://localhost:3000` in your browser.
7. Keep the terminal running while you use the website. Press `Ctrl + C` in the terminal to stop it.

## Demo administrator login
- Email: `admin@abhsports.pk`
- Password: `ABHadmin123!`

Click **ADMIN** in the header. The admin can view product/order totals, edit product name, image URL, price and stock, add/delete products, review order history, and update order status.

**Security note:** These are development/demo credentials, not suitable for a public production store. Before deployment, set strong secrets using environment variables `ADMIN_EMAIL` and `ADMIN_PASSWORD`, and add proper password hashing, persistent sessions, CSRF protection, validation, and HTTPS. The current admin session tokens are held in memory and expire when the server restarts.

## What is included
- System architecture diagram in `ARCHITECTURE.svg` and a report-ready Mermaid version in `PROJECT_REPORT.md`.
- 60 seeded cricket products across Bats, Batting Gloves, Batting Pads, Guard, Wicketkeeping, Helmets, Caps, Kit Bag, and Shoes.
- Bats include English Willow and Kashmir Willow subcategories.
- Search, category filters, price ceiling, availability filter, sorting and animated category switching.
- Product detail modal with description, stock state, size/colour selectors and quick add. Size/colour options are demo selections; inventory is tracked at product level.
- Wishlist/saved items stored in the browser.
- Shopping bag with variant-labelled lines, quantity controls and a saved browser cart.
- Checkout with country/region, name, email, address, city, phone, landmark, newsletter and save-details options; Cash on Delivery / demo Online Payment selection.
- Shipping fee of Rs. 350 for orders below Rs. 10,000 and free shipping at or above Rs. 10,000.
- Customer order lookup using order reference plus checkout phone number.
- Demo newsletter signup stored locally in the browser; no email is sent.
- Local category artwork that works without remote product-image dependencies; admin can set a product image URL.
- Orders saved to `data/orders.json` and stock changes saved to `data/products.json`.
- Admin product and stock controls, order history, and status updates.
- Responsive black/charcoal, red and white performance design with sporty transitions and reduced-motion support.

## Data storage
This coursework version stores records in JSON files under `data/`. It is easy to inspect for a class demo, but is not a replacement for a database on a real store. Keep backups of the `data` folder. The app seeds its initial 60 products the first time it runs; after that, existing `products.json` is preserved.

## Payment and shipping limitations
The Online Payment option is a demonstration choice only. It does not collect card details or process a payment. No real shipping provider is connected. Do not enter real sensitive payment information.

## Project structure
```text
ABH-SPORTS-Ecommerce-Project/
├── data/
│   ├── products.json       # created automatically on first run
│   ├── orders.json         # created automatically on first run
│   └── users.json          # reserved for future extension
├── public/
│   ├── index.html          # store, cart, checkout, admin interface
│   ├── styles.css          # layout and theme
│   └── app.js              # browser-side interactions
├── server.js               # Express API, stock and order logic
├── package.json
├── PROJECT_REPORT.md
├── ARCHITECTURE.svg
└── README.md
```

## Quick test checklist
1. Open the landing page and verify all ten categories appear.
2. Search for “willow” and confirm matching bats appear.
3. Change category and price slider; the visible catalogue should update.
4. Add an in-stock product to the bag and change quantity.
5. Place a test order using fictional contact details and Cash on Delivery.
6. Sign in as admin and check the order appears in **ORDER HISTORY**.
7. Change an order status and update a product name, image URL, price and stock.
8. Copy the order reference, open Track Order and verify using the checkout phone number.
9. Refresh the store and confirm saved product stock and orders remain.
10. Test a product with stock zero and attempt to order more than the available quantity.


## Visual theme update
The storefront uses a dark black/charcoal base with white typography and red highlights. Product-category switching has a short sporty slide-in animation, with staggered product cards and reduced-motion support.


## Reference and originality
The shopping flow and broad storefront patterns were informed by the public Miandad Sports website. ABH SPORTS branding, copy, layout implementation and local category illustrations are original for this coursework project; this package does not include Miandad Sports private code, brand assets or product catalogue.


## Homepage design update
The homepage now includes a three-slide promotional hero, service highlights, popular category cards, new-arrival and featured-product sections, a promotional shipping band, the full searchable catalogue, newsletter demo, and store information. The layout is inspired by common cricket retail storefront patterns seen on Miandad Sports, with original ABH SPORTS branding and a black/red/white visual identity.
