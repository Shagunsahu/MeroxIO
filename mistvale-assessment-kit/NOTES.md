Assessment Notes
1. What I Changed
Bugs Fixed & Business Rules Enforced
R1 (Price source of truth): Removed DOM text parsing. Prices are fetched directly from PRODUCTS. Fixed comma parsing bug where "1,299" parsed to 1.

R2 (Purchase limits): Enforced max 5 units/item limit and stock bounds. Fixed string concatenation bug ("1" + 1 = "11"). Disabled add-to-cart for sold-out items.

R3 (Coupon WELCOME10): Updated logic: case-insensitive, minimum ₹399 subtotal (excluding "Gifts" category), max ₹150 cap, non-cumulative application.

R4 (Shipping): Set free shipping threshold to ₹499 after discount with dynamic progress bar (flat ₹49 shipping otherwise).

R5 (Formatting): Implemented formatINR() with Indian digit grouping (₹1,23,456) and rounded final order total to the nearest rupee.

R6 (Sold-out order): Updated sort comparators to force out-of-stock items (stock === 0) to always appear last.

R7 (Unified state): Combined search, category, and sort state into one function applyFiltersAndSort(). Added debounce (250ms) and request-ID tracking to fix search race conditions.

R8 (Pincode error handling): Added client-side regex check, caught promise rejections (INVALID_PINCODE), and added .finally() block to prevent UI freeze.

Cart fixes: Fixed null handling on initial localStorage load, cart.splice(i, 1) array removal, and stacked event listeners.

Design, UX & Technical Polish
Brand System (BRAND.md): Applied official palette (#1f3d2b, #4f7942, #f6f1e7, #d9962b). Replaced outdated fonts with Fraunces (headings) and Inter (body).

Hero & Card UI: Centered hero banner with dual CTAs matching brand specs. Applied 88% grayscale tint and disabled styling to sold-out card grid items.

Quick View: Widened modal to 760px and removed internal scrollbars for seamless viewing.

Clean Architecture: Purged jQuery, animate.css, and Font Awesome. Used native Vanilla JS, CSS Grid/Flexbox, and inline SVGs.

Contract & SEO: Preserved <form id="checkout-form"> contract and legal footer verbatim. Added full metadata and JSON-LD schemas (Organization, Product, FAQPage).

2. What the AI Got Wrong
Fabricated Social Proof: AI initially generated fake claims ("4.9/5 by 10,000+ customers", "Shark Tank India"). Removed them per Constraint 7.

Bypassed Checkout Contract: AI replaced the checkout form submission with an API fetch(). Restored native form submission with JSON-serialized inputs per Constraint 4.

Flawed Coupon Logic: AI applied discounts to "Gifts" items. Fixed by filtering out non-eligible categories prior to discount calculation.

Incorrect Search Index Filter: AI used ids.indexOf(p.id), which dropped product ID at index 0 (0 is falsy). Fixed using ids.includes(p.id).

3. Images
Hero Banner: Generated via Gemini / Imagen 3 (1600×900 WebP, 207 KB).

Product Images (p101–p108): Generated via Gemini / Imagen 3 with consistent studio lighting and matching tea ingredients (800×800 WebP, 58–94 KB each).

Logo: Clean scalable vector SVG (images/logo.svg, 1.5 KB) with high-DPI PNG fallback.

4. How I Tested It
Automated Logic Tests: Verified zero library dependencies, coupon math edge cases, gift exclusions, and sold-out sorting using Node.js.

Responsive Layout: Tested at 360px, 480px, 768px, 1024px, and 1200px+ (2 columns on mobile, 4 on desktop).

Accessibility: Verified keyboard tab focus rings (--saffron), ESC-key modal closing, and ARIA attributes.

5. Questions for the Team
Free Shipping Threshold: Banner said ₹499 while old JS code said > 599. Standardized implementation to ₹499 post-discount.

Legal Footer Typo: Left "© 2020 MistVale. All right reserved." unchanged per Constraint 6.

Pincode Delivery: Unmapped valid pincodes resolve to non-serviceable. Should fallback express shipping be offered for these areas?

6. Time Spent & Extra Features Added
Time Spent: ~3.5 hours total.

Bonus Extensions:

Size selector options (100g / 250g) in Quick View.

Persistent Wishlist saved to localStorage (mv_wishlist).

Shareable URL query parameters for active filters (URLSearchParams).

Non-intrusive toast notifications.

Gift message input at checkout.

Recently viewed items slider (mv_recently_viewed array, max 4 items).