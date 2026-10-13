# Wonderxasia B2B Agri-Export Platform — Fullstack Delivery

## 1. Node.js & Express Backend Architecture
- **Server:** Built robust Node.js + Express backend (`server.js`) listening on port 3000.
- **REST APIs:**
  - `GET /api/health` — Server uptime and system diagnostics.
  - `GET /api/categories` — Returns 8 distinct commodity families with descriptions and specs.
  - `GET /api/categories/:slug` — Returns category details and all associated commodities.
  - `GET /api/products` — Full product catalog with real-time search, category filtering, and sorting.
  - `GET /api/products/:slug` — Comprehensive technical specifications matrix and related products.
  - `POST /api/inquiries` — Validates RFQs and inquiries, assigns unique tracking IDs (`WXA-RFQ-XXXX`), and persists to `data/inquiries.json`.
  - `GET /api/inquiries/stats` — Real-time trade statistics and live activity counter.
  - `POST /api/newsletter` — Market trade bulletin subscription endpoint.

## 2. Multi-Page Architecture
Replaced the single-page layout with dedicated, deep-linked pages:
- **Home (`/`):** Luxury hero banner, animated stats, interactive live ticker, 8 category showcase, flagship products, export process overview, and RFQ callouts.
- **Categories Hub (`/categories`):** Master directory dividing 40+ products into 8 distinct export families.
- **Single Category (`/category/:slug`):** Dynamic category view rendering only products belonging to that category with technical export guidelines.
- **Products Catalog (`/products`):** Interactive searchable directory with real-time category filter pills, sorting dropdown, and quick quote actions.
- **Product Detail (`/product/:slug`):** Technical specification matrix (origin, grades, purity, moisture, HS code, shelf life, packaging options, and related products).
- **About Us (`/about`):** Wonderx Innovations company profile, Indian sourcing heritage, and operational pillars.
- **Export Process (`/process`):** 6-stage logistics pipeline from mandi procurement to Nhava Sheva/Mundra port container stuffing and BL issuance.
- **Quality & Standards (`/quality`):** Laboratory safety protocols (HPLC Aflatoxin, Sudan dye test, pesticide MRLs), export certificates, and sample request policy.
- **Interactive RFQ Builder (`/rfq`):** 4-step interactive quote builder with real-time summary connected to `/api/inquiries`.
- **Contact Trade Desk (`/contact`):** Direct contact form connected to backend, office details, and port operations.
- **404 Page (`/404`):** Custom error page.

## 3. Product Categorization
Strictly organized all 40+ shelf-stable commodities into 8 distinct families:
1. **Whole Spices & Seeds (14 varieties):** Cumin, Dry Red Chilli, Turmeric Fingers, Coriander Seeds, Black Pepper, Green Cardamom, Fennel, Fenugreek, Cloves, Cinnamon, Star Anise, Ajwain, Black Mustard, White Pepper.
2. **Ground & Powdered Spices (7 varieties):** Turmeric, Red Chilli, Cumin, Coriander, Ginger, Cardamom powders, Chilli Flakes.
3. **Blended Masalas & Seasonings (5 blends):** Garam Masala, Biryani Masala, Meat/Chicken Masala, Chaat Masala, Tandoori Masala.
4. **Basmati Rice & Grains (Aged Reserve):** Aged Traditional and 1121 Basmati Rice.
5. **Pulses, Lentils & Beans (5 varieties):** Masoor Dal, Kabuli Chickpeas (42-44 count), Rajma, Moong, Urad.
6. **Nuts & Dried Fruits (3 commodities):** Cashew Kernels (W240/W320), Almonds, Golden Raisins.
7. **Edible Oils & Natural Sweeteners (3 items):** Cold-pressed Sesame and Mustard oils, Organic Jaggery.
8. **Packaged Pantry Foods (2 ranges):** Savoury snacks and shelf-stable packaged foods.

## 4. Visual, Interactive & Motion Enhancements
- **Luxury Color Palette:** Deep Imperial Forest (`#041411` / `#08211b`), radiant Saffron Gold (`#de8c1a` / `#f5a623`), crisp Emerald Mint (`#10b981`), and warm off-white linen (`#fcfbf7`).
- **Interactive RFQ Basket:** Persistent cart in `localStorage` allowing buyers to add commodities as they browse and open an off-canvas drawer to review quantities.
- **Animations:** Scroll-triggered smooth fade-ups, animated numbers counters, floating ambient hero particles, and periodic live buyer activity toasts.

## 5. Commercial & Promotional Banner Suite (V3 Upgrade)
Added comprehensive B2B banners throughout the site:
- **Top Promotional Announcement Bar (`.promo-top-bar`):** High-visibility gold/forest campaign banner with live pulse, current harvest booking window alert, direct RFQ rate card link, and sample kit button.
- **Full-Width 4-Slide Hero Banner Slider (`.hero-slider-section`):** High-impact interactive hero carousel with smooth transitions, autoplay (5.5s), pause on hover, touch swipe, prev/next circular nav, and slide pagination counter (`01 / 04`). Covers Whole Spices (Mandi Origin), Cryo-Milled Ground Powders (Zero Sudan Dye), Aged Himalayan Basmati & Chickpeas, and Bespoke Masalas & OEM Private Labeling.
- **Promotional Split Category Banners Grid (`.promo-banners-section`):** 3 visual category showcase banners (Whole Spices, Cryo Powders, Aged Basmati) with hover zoom, feature pills, and direct category links.
- **Mid-Page Wide Commercial Campaign Banner (`.wide-campaign-banner`):** Expansive feature banner highlighting Direct Mandi-to-Port Container Contracts, OEM Private Labeling (100g to 50kg), SGS inspection, and live JNPT/Mundra export desk metrics.
- **Free Export Sample Kit Lead-Gen Banner (`.sample-kit-banner`):** High-conversion lead magnet offering 250g certified samples with DHL dispatch and HPLC Certificate of Analysis.
- **Pre-Footer Full-Width Conversion Banner (`.pre-footer-banner`):** Final call-to-action banner driving RFQ submissions, instant WhatsApp desk chats, and phone consultations.
- **In-Page Category & Catalog Promotional Strips (`.page-promo-strip`):** Seasonal sourcing banners embedded directly within product catalog and category hubs.

