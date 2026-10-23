# TurkMart — E-commerce starter prototype

A responsive storefront prototype for a multi-seller marketplace focused on Lodwar and wider Turkana County, Kenya. It is intentionally built with plain HTML, CSS and JavaScript so a beginner can inspect and run it without installing a framework.

## Run it locally

1. Extract the ZIP folder.
2. Open `index.html` in a modern browser. For a more reliable local preview, use VS Code with the Live Server extension.
3. Try searching, filtering categories, sorting, viewing product details, adding/removing products, saving wishlist items, changing cart quantities, and submitting a demo checkout.

## Lodwar/Turkana focus

- Local-first messaging and delivery address prompts
- A sample Local Turkana category for artisan products
- Marketplace direction: independent sellers list products; seller verification, stock accuracy, delivery and returns must be implemented in the production backend
- Sample products, prices and imagery are placeholders, not verified offers from real Lodwar sellers

## What's implemented

- Responsive product storefront and category filters
- Search and sorting
- Product detail modal
- Cart quantities, subtotal, delivery estimate and totals
- Wishlist
- Demo checkout form with basic client-side validation
- Cart, wishlist and demo orders saved in the current browser's localStorage

## Important limitations — not production-ready yet

This is a front-end prototype, not a live commerce platform. Product images load from Unsplash and require an internet connection. Product descriptions, prices, ratings, brand references and inventory are sample content and must be verified/replaced. Customer information and demo orders stay in local browser storage and are not sent to a business. There is no server, shared database, real authentication, admin portal, inventory reservation, transactional email, or payment integration. The M-Pesa/card choices are labels only; no money can be charged. Do not use this prototype to collect real customer data or claim an order was placed.

## Recommended production architecture

- Frontend: Next.js + TypeScript, responsive accessible UI
- Backend: Next.js server actions/API or a separate Node.js service
- Database: PostgreSQL with migrations and backups
- Authentication: managed auth or secure server-side sessions; role-based admin access
- Payments: Safaricom Daraja STK Push for M-Pesa, with server-side callback verification and idempotent payment/order state handling. Add a card provider only after merchant onboarding.
- Email/SMS: provider integration for order receipts and status notifications
- Deployment: managed application hosting, managed database, custom domain, HTTPS, logging, monitoring and backup plan

## Production milestones

1. Confirm business name, target products, sourcing, real prices, stock, delivery coverage, returns/refunds policy and support contact.
2. Create a database schema for products, variants, stock movements, users, addresses, carts, orders, order items, payment attempts and audit events.
3. Implement server-side validation, authentication, admin roles, rate limiting, CSRF protections where applicable, safe secrets handling, and privacy controls.
4. Integrate M-Pesa in sandbox first. Verify callbacks on the server; never trust a browser redirect as proof of payment. Use idempotency to prevent duplicate orders or charges.
5. Test checkout edge cases, low stock, duplicate callbacks, failures, refunds, mobile layouts, accessibility and backups.
6. Deploy staging, complete test transactions, configure domain and HTTPS, then launch after a security review.

## Before we continue

Before launch, confirm business ownership and registration needs with a qualified local adviser, seller onboarding rules, commission model, delivery coverage, real product prices, support contact, domain, and Safaricom Daraja merchant onboarding. Do not share passwords, API secrets or payment credentials in chat. Do not share passwords, API secrets or payment credentials in chat.

## Turkana-inspired visual identity

The storefront uses a palette inspired by Turkana landscapes and beadwork: terracotta/sunset orange, deep teal, warm sand, and olive accents. A bundled locally referenced banner concept (`turkana-inspired-banner.png`) is used in the hero so the page does not depend on an external hero image. This is a design concept, not a claim that the image depicts a verified local scene or community member.
