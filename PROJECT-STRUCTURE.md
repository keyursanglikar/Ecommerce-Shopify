# Posterized.in — Full Shopify 2.0 Theme Architecture

This project is structured according to the official **Shopify Online Store 2.0 (OS 2.0)** standard.
The code editor inside Shopify uses this exact layout (identical to VS Code).

---

## 📂 Project Structure Overview

```text
├── layout/                           # Master HTML Shells
│   ├── theme.liquid                  # Primary layout loaded for all storefront pages
│   └── password.liquid               # Coming-soon / pre-launch lock screen
│
├── templates/                        # Page routing and section order (JSON templates)
│   ├── index.json                    # Homepage layout (defines order of sections)
│   ├── product.json                  # Default Product Detail Page (PDP)
│   ├── product.custom-print.json     # Custom photo uploader poster template
│   ├── collection.json               # Category listing & product catalog grid
│   ├── cart.json                     # Dedicated cart page
│   ├── search.json                   # Search results page
│   └── 404.json                      # 404 Not Found error page
│
├── sections/                         # Modular & Reusable Components (Liquid + Schema)
│   │   # --- EXACT POSTERIZED.IN SECTIONS ---
│   ├── pz_home_hero.liquid           # Hero banner + UGC customer wall review ticker
│   ├── pz_home_packs.liquid          # Pre-curated Room Wall Setup Packs
│   ├── pz_home_byw.liquid            # "Build Your Wall" custom interactive collage builder
│   ├── pz_home_mm.liquid             # "Mix & Match" offers (Buy 4 Get 3 / Buy 5 Get 5)
│   ├── pz_home_colhead.liquid        # Collection header & category filters
│   ├── pz_home_row_3pc.liquid        # 3-Piece Split Poster sets
│   ├── pz_home_row_4pc.liquid        # 4-Piece Split Poster sets
│   ├── pz_home_row_5pc.liquid        # 5-Piece Split Poster sets
│   ├── pz_home_row_8pc.liquid        # 8-Piece Panoramic Split Art sets
│   ├── pz_home_custom.liquid         # "Transform your memories into art" print uploader
│   ├── pz_home_trust.liquid          # Social proof: "Why 500,000+ walls chose us"
│   │   # --- CORE STORE SECTIONS ---
│   ├── header.liquid                 # Navigation bar, mobile menu, search, cart icon
│   ├── footer.liquid                 # Links, payment badges, newsletter, copyright
│   ├── offer-marquee.liquid          # Scrolling discount ticker
│   ├── story-categories.liquid       # Instagram-style circular category bubbles
│   ├── split-art-showcase.liquid     # Multi-panel art showcase
│   └── custom-print-builder.liquid   # Live file upload with frame preview
│
├── snippets/                         # Lightweight partials & reusable UI widgets
│   ├── poster-sticky-mobile-bar.liquid # Bottom sticky "BUY NOW" bar for mobile
│   ├── card-product.liquid           # Poster card with hover flip, price, badges
│   ├── cart-drawer.liquid            # Slide-out AJAX cart drawer
│   ├── buy-buttons.liquid            # Add to cart & buy now triggers
│   ├── swatch-input.liquid           # Size swatches (A4, A3, 12x18)
│   └── meta-tags.liquid              # SEO, OpenGraph & social sharing meta tags
│
├── assets/                           # Static assets, compiled stylesheets, scripts
│   ├── pz-home.css                   # Exact styling & animations from posterized.in
│   ├── base.css                      # Global theme typography, layout & resets
│   ├── section-story-categories.css  # Story category bubble styling
│   ├── cart-drawer.js                # AJAX drawer sliding logic
│   └── global.js                     # Core theme utilities & event listeners
│
├── config/                           # Global store & theme configuration
│   ├── settings_schema.json          # Admin customization controls (colors, fonts)
│   └── settings_data.json            # Active store settings & selected color palette
│
└── locales/                          # Localization & translations
    └── en.default.json               # Default English strings
```

---

## 🛠️ The Tech Stack (Official Shopify Standard)

| Layer | Technology | Purpose |
| :--- | :--- | :--- |
| **Templating Engine** | **Liquid** (Shopify OS 2.0) | Renders dynamic product data, cart objects, loops, filters |
| **Page Configuration** | **JSON Templates** (`index.json`) | Defines section ordering, settings, and modular blocks |
| **Styling** | **Modern CSS3 & Flexbox/Grid** | Fully responsive layout (2 cols on mobile, 4 on desktop) |
| **Typography** | **Google Fonts (Barlow & Barlow Condensed)** | Exact fonts used by Posterized for headers and badges |
| **Client-Side Scripting** | **Vanilla JavaScript (ES6+)** | Lightweight, zero-dependency AJAX cart and interactions |
| **Cart & API** | **Shopify AJAX Cart API** | Asynchronous cart addition (`/cart/add.js`, `/cart.js`) |

---

## 🚀 How to Edit Directly in the Shopify Code Editor

1. Open your Shopify Code Editor (the screen matching VS Code in your browser).
2. To modify any section:
   * **Hero & Marquee:** Open `sections/pz_home_hero.liquid` or `sections/offer-marquee.liquid`.
   * **Custom Artwork Uploads:** Open `sections/custom-print-builder.liquid`.
   * **Split Poster Layouts:** Open `sections/pz_home_row_3pc.liquid` or `sections/split-art-showcase.liquid`.
   * **Styling & Colors:** Open `assets/pz-home.css`.
3. Hit `Ctrl + S` (or click **Save**) to save changes instantly.
