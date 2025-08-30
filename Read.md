# SA Fashion — Landing Page

Pixel-faithful recreation of the provided fashion page.  
Built with **semantic HTML**, **modern CSS**, and **vanilla JS** (inline in `index.html`). Fully responsive (mobile, tablet, desktop). Cart state persists in `localStorage`.

## Project Structure

Code/
├─ index.html # Markup + inline JavaScript (cart, drawer, toast, smooth scroll)
├─ styles.css # Layout, typography, responsiveness
├─ Read.me # This file



## How to Run
- Open `index.html` directly in a browser, **or**
- Serve locally (any static server). Example:
  - Python 3: `python -m http.server` → http://localhost:8000

## Features
- Hero with “Shop Now” CTA (left) and model image (right).
- Feature bar (Shipping / 14 Days / Security / 24/7) positioned **below** the CTA.
- “Trending Products” grid with **cart button** on each card (adds to cart).
- Slide-in **Cart drawer** (open from header cart icon): add/remove, clear cart, live totals, persisted via `localStorage`.
- Two promo banners (“Summer Collection” and “What’s New?”).  
  _Note: “Buy 1 Get 1” intentionally removed per requirements._
- Newsletter input (demo toast; no backend).
- Social icons link to official **Instagram / Facebook / WhatsApp Web** login pages (open in new tab).
- Stacked serif **“SA”** monogram to match the reference.

## Breakpoints
Responsive layout closely follows the design:

- **Desktop (≥ 1024px)**
  - Hero 2-column; Features 4 cols; Products 3 cols; Banners 2 cols; Cart drawer 320px.
- **Tablet (640–1023px)**
  - Hero 1-column; arrows hidden; Features 2 cols; Products 2 cols; Banners stacked.
- **Mobile (≤ 639px)**
  - Features 1 col; Products 2 cols; larger tap targets; Cart drawer 92vw.
- **Small phones (≤ 420px)**
  - Products 1 col; slightly smaller SA monogram and headings.

_Breakpoints live in `styles.css` within the `@media (max-width:1023px)`, `639px`, and `420px` blocks._

## Accessibility
- Proper landmarks (`header`, `main`, `footer`) and labels.
- Alt text on all images; buttons for interactive controls.
- “Skip to content” link for keyboard users.
- Toast uses `role="status"` for polite announcements.
- Drawer toggles `aria-hidden` on open/close.

## Performance Notes
- No JS frameworks; inline SVG icons.
- Google Fonts: Poppins + Playfair Display (for the logo).
- Images use Unsplash CDN. Replace with brand assets when available.

## Assumptions
- Products are static in the HTML (no backend). Cart is client-side only.
- Checkout flow and full search are **out of scope**.
- Copy, prices, and product images are placeholders resembling the reference.

## Editing Content
- **Products:** Duplicate or edit `<article class="card">` inside `#productGrid`. Update `data-id`, `data-price`, `<img src>`, and the title text.
- **Features:** Edit the four `<article class="feature">` blocks.
- **Banners:** Update images/text inside the two `.banner` elements.
- **Logo size:** Tweak `.logo-mono` and `.logo-mono .s/.a` in `styles.css`.

## Browser Support
Latest **Chrome**, **Edge**, **Firefox**, and **Safari** (desktop & mobile). IE not supported.

## Known Enhancements (optional)
- Add **Esc to close** cart drawer and focus-trap within the drawer.
- Wire newsletter form to a backend endpoint.
- Replace CDN images with optimized, locally hosted assets.
