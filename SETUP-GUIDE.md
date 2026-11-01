# Posterized.in Shopify Theme Clone — Setup & Launch Guide

This repository contains the complete custom Shopify 2.0 theme built to replicate the **Posterized.in** poster & wall decor storefront experience.

---

## 1. Quick Installation into Shopify

1. Log into your **Shopify Admin** (`https://admin.shopify.com`).
2. Navigate to **Online Store** > **Themes**.
3. Under the **Theme library** section, click **Add theme** > **Upload zip file**.
4. Upload the generated **`posterized-theme.zip`** from this directory:
   ```
   f:\FREELANCE\SOFTGENIX-IT-SOLUTIONS\Ecommerce-Shopify\posterized-theme.zip
   ```
5. Click **Actions > Publish** (or click **Customize** to preview first).

---

## 2. Key Custom Posterized Sections Built In

### 1. **Offer Marquee Ticker** (`sections/offer-marquee.liquid`)
* Continuous animated marquee banner displaying high-converting deals:
  * `🔥 BUY 4 GET 3 FREE (Auto Applied at Checkout)`
  * `⚡ BUY 5 GET 5 FREE`
  * `🚀 FREE SHIPPING ON ALL PREPAID ORDERS`
  * `🖼️ 300 GSM MATTE FINISH WITH FREE WALL TAPE`
* Fully editable text, emojis, background color, and text color directly in the Shopify theme visual editor.

### 2. **Instagram-Style Story Categories** (`sections/story-categories.liquid` + `assets/section-story-categories.css`)
* Mobile-first horizontal scrolling circular categories with gradient border rings and badges:
  * **Anime** (`HOT`)
  * **F1 & Cars** (`TREND`)
  * **Split Sets** (`POPULAR`)
  * **Gym & Quotes**
  * **Gaming**
  * **Custom Prints** (`NEW`)

### 3. **Custom Photo Print Builder** (`sections/custom-print-builder.liquid` + `templates/product.custom-print.json`)
* Dedicated customizer page/template for personalized prints.
* Features:
  * Direct photo upload field with live frame mockup preview.
  * Custom caption / song name text field.
  * Size selector swatches (`A4: 8.3x11.7 in`, `A3: 11.7x16.5 in`, `12x18 in`).
  * Direct pass-through to Shopify order line-item properties (`properties[Uploaded Image]`).

### 4. **Split Wall Art Sets Showcase** (`sections/split-art-showcase.liquid`)
* Dedicated multi-panel visual grid showcasing 3-Piece, 4-Piece, and 8-Piece wall splits.
* Interactive card styling with panel split dividers and dimension tags.

### 5. **High-Converting Sticky Mobile "Buy Now" Bar** (`snippets/poster-sticky-mobile-bar.liquid`)
* Fixed bottom checkout bar on mobile devices that triggers the instant add-to-cart/buy workflow when browsing product details.

---

## 3. Product Setup & Pricing Strategy (Matching Posterized)

### Product Options & Variants:
* **Option 1: Size**
  * `A4` (₹199 - ₹249)
  * `A3` (₹349 - ₹399)
  * `12x18 inch` (₹449 - ₹499)
* **Option 2: Frame / Tape**
  * `Frameless (Pre-applied tape included)` [Default]
  * `Black Wood Minimalist Frame` (Upsell +₹350)

### Assigning Customizer to a Product:
1. Create a product named **"Custom Poster / Photo Print"** in Shopify Admin.
2. In the right-hand sidebar under **Theme template**, select **`custom-print`**.
3. Save. Customers can now upload their pictures directly on this product page.

---

## 4. Automatic Discounts Setup ("Buy 4 Get 3 Free")
Posterized uses automatic volume discounts:
1. In Shopify Admin, go to **Discounts** > **Create discount** > **Buy X get Y**.
2. Select **Automatic discount**.
3. Title: `Buy 4 Get 3 Free`.
4. Customer buys: `Quantity 7` of posters.
5. Customer gets: `Quantity 3` at `100% off` (Free).
6. Set eligible items to **Specific collections** (e.g., Single Posters).

---

## 5. Recommended Apps for Full Match
* **Payment Gateways:** Razorpay / Cashfree / PhonePe (for 0% UPI failure rates in India).
* **Reviews with Wall Photos:** Judge.me (Free tier available).
* **COD Verification & Fast Checkout:** Fastrr or UpPromote.
