# Manual smoke-test checklist

- [ ] Open `index.html`; verify home, 8 shops, categories and product cards render.
- [ ] Search for `rice`, `Grocery`, and `Green Basket`; verify results update without reload.
- [ ] Explore filters: category, max price, minimum rating, distance, stock and sort order.
- [ ] Open a shop, open a product, adjust quantity and add it to cart.
- [ ] Change cart quantities, remove an item and clear the cart.
- [ ] Sign in as customer; checkout one shop's items with COD and with UPI placeholder; verify order ID and order history.
- [ ] Sign in as seller; create/edit/delete a product, change stock, edit shop settings and update an order status.
- [ ] Refresh; verify LocalStorage state persists. Log out and log in again.
- [ ] Test theme, manual location and geolocation denial fallback.
- [ ] Test at 320px wide and desktop widths.
- [ ] Deploy to HTTPS GitHub Pages; confirm manifest and service worker load and app can be installed.

These are manual checks provided with the project; no browser automation environment was available during generation.
