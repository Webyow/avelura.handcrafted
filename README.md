# Avelura Handicrafts — Premium storefront demo

A responsive, multi-page front-end e-commerce prototype built with HTML, CSS, vanilla JavaScript and Tailwind CSS CDN.

## Run
Open `index.html` in a browser, or run a local static server from this directory:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000.

## Pages
- `index.html` — home, brand story, collections, newsletter
- `shop.html` — product listing, category filter via query string, sorting
- `product.html?id=1` — product details, quantity, wishlist, cart and customer reviews
- `cart.html` — editable cart and totals
- `wishlist.html` — saved products
- `checkout.html` — demo delivery form and order placement
- `account.html` — local demo order history
- `admin.html` — local product CRUD, image upload, inventory, order status

## Local data
The demo stores products, cart, wishlist, reviews and orders in browser `localStorage` under keys prefixed `av_`. Admin image uploads are converted to data URLs and stored locally. Keep uploaded images below 2.5 MB to avoid browser storage limits. Use a browser's site-data clear option to reset the demo.

## Notes
- No backend, authentication server, database, or real payment gateway is connected.
- Checkout is a simulation. It does not charge customers or dispatch orders.
- The admin page is a demonstration interface, not secure production administration.
- Tailwind CSS and Google Fonts load from CDNs; an internet connection is needed for those external resources and the sample product photography.
- Replace sample product photography, descriptions, contact details and prices with client-approved content before presenting as a live store.


## Free WhatsApp order notification demo

The checkout creates a pre-filled WhatsApp message for the Avelura number **+91 93903 15117**. On order submission, the browser attempts to open WhatsApp with the order ID, customer details, delivery address, line items, shipping and total. The sender must tap **Send** in WhatsApp; a static front-end website cannot silently send a message. If the browser blocks the new tab, the confirmation page includes a Send order on WhatsApp link. This uses the free `wa.me` click-to-chat flow and does not require a WhatsApp API or backend.
