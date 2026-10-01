# Mistvale Tea Co. — AI Prompt Log

This document records the exact prompts used during the rescue and redesign of the Mistvale Tea Co. store, including code generation, asset creation, and iterations.

---

## Prompt 1
- Tool: Gemini / Imagen 3
- Type: image
- Prompt:
  > Serene morning landscape of Darjeeling tea estate terraces veiled in soft gentle mist at dawn. Calm rolling green hills with lush tea bushes, soft golden sunrise light filtering through fog, subtle blue misty mountain ridges in the background. Cinematic, peaceful, premium, earthy aesthetic, natural soft lighting, no people, no text.
- Outcome: accepted
- Why: Produced an evocative, calm landscape perfectly capturing the brand aesthetic ("like a quiet tea garden at dawn"). Converted and compressed to WebP at 207 KB to strictly satisfy the < 250 KB constraint.

---

## Prompt 2
- Tool: Gemini / Imagen 3
- Type: image
- Prompt:
  > Artisanal tea packaging studio photograph: an elegant dark forest green cylindrical matte tea tin on a warm neutral linen and cream stone surface, next to a small ceramic saucer holding dry granular malty CTC black tea leaves. Soft natural morning window light, subtle soft shadow, minimalist luxury organic tea brand, clean composition, 1:1 square framing, no text on packaging.
- Outcome: accepted
- Why: Established the core visual design language for product packaging: matte dark green tin, cream linen/stone tabletop, consistent side lighting, and realistic loose CTC leaves for Assam Breakfast Black Tea (p101).

---

## Prompt 3
- Tool: Gemini / Imagen 3
- Type: image
- Prompt:
  > Artisanal tea packaging studio photograph: an elegant dark forest green cylindrical matte tea tin on a warm neutral linen and cream stone surface, next to a small ceramic saucer holding delicate whole loose Darjeeling first flush tea leaves with silvery tips. Soft natural morning window light, subtle soft shadow, minimalist luxury organic tea brand, clean composition, 1:1 square framing, no text on packaging.
- Outcome: accepted
- Why: Seamless consistency with Prompt 2, accurately featuring delicate whole orthodox spring harvest leaves with silvery tips for Darjeeling First Flush (p102).

---

## Prompt 4
- Tool: Gemini / Imagen 3
- Type: image
- Prompt:
  > Artisanal tea packaging studio photograph: an elegant dark forest green cylindrical matte tea tin on a warm neutral linen and cream stone surface, next to a small ceramic saucer holding green tea leaves blended with red saffron strands, whole green cardamom pods, cinnamon bark pieces, and slivered almonds. Soft natural morning window light, subtle soft shadow, minimalist luxury organic tea brand, clean composition, 1:1 square framing, no text on packaging.
- Outcome: accepted
- Why: Accurately represented all botanical ingredients mentioned in the product description (green tea, saffron, cardamom, cinnamon, slivered almonds) for Kashmiri Kahwa (p103).

---

## Prompt 5
- Tool: Gemini / Imagen 3
- Type: image
- Prompt:
  > Artisanal tea packaging studio photograph: an elegant dark forest green cylindrical matte tea tin on a warm neutral linen and cream stone surface, next to a small ceramic saucer holding rich black tea leaves mixed with crushed ginger pieces, green cardamom pods, whole cloves, and black peppercorns. Soft natural morning window light, subtle soft shadow, minimalist luxury organic tea brand, clean composition, 1:1 square framing, no text on packaging.
- Outcome: accepted
- Why: Produced authentic-looking spiced chai ingredients matching Masala Chai Blend (p104) while maintaining identical camera framing and lighting.

---

## Prompt 6
- Tool: Gemini / Imagen 3
- Type: image
- Prompt:
  > Artisanal tea packaging studio photograph: an elegant dark forest green cylindrical matte tea tin on a warm neutral linen and cream stone surface, next to a small ceramic saucer holding fresh whole rolled emerald-green tea leaves. Soft natural morning window light, subtle soft shadow, minimalist luxury organic tea brand, clean composition, 1:1 square framing, no text on packaging.
- Outcome: accepted
- Why: Accurately reflected smooth, grassy rolled green tea leaves for Nilgiri Green Tea (p105).

---

## Prompt 7
- Tool: Gemini / Imagen 3
- Type: image
- Prompt:
  > Artisanal tea packaging studio photograph: an elegant dark forest green cylindrical matte tea tin on a warm neutral linen and cream stone surface, next to a small ceramic saucer holding whole dried yellow chamomile flowers and dried green holy basil tulsi leaves. Soft natural morning window light, subtle soft shadow, minimalist luxury organic tea brand, clean composition, 1:1 square framing, no text on packaging.
- Outcome: accepted
- Why: Rendered dried chamomile blossom heads and holy basil leaves for Chamomile & Tulsi herbal blend (p106).

---

## Prompt 8
- Tool: Gemini / Imagen 3
- Type: image
- Prompt:
  > Artisanal tea packaging studio photograph: an elegant dark forest green cylindrical matte tea tin on a warm neutral linen and cream stone surface, next to a small ceramic saucer holding vibrant deep crimson dried hibiscus petals and fragrant dried pink rose petals. Soft natural morning window light, subtle soft shadow, minimalist luxury organic tea brand, clean composition, 1:1 square framing, no text on packaging.
- Outcome: accepted
- Why: Captured deep ruby hibiscus calyces and dried rose petals for Hibiscus Rose Infusion (p107) with vibrant natural color.

---

## Prompt 9
- Tool: Gemini / Imagen 3
- Type: image
- Prompt:
  > Artisanal tea packaging studio photograph: an open handcrafted natural wooden gift box showcasing six small dark green tea tins neatly arranged inside, accompanied by a small minimalist parchment brewing guide card. Resting on a warm neutral linen and cream stone surface with soft morning window light, subtle soft shadow, luxury organic tea gift set, clean composition, 1:1 square framing, no text on packaging.
- Outcome: accepted
- Why: Exactly matched the description of the Tea Lover's Sampler Gift Box (p108) with six curated tins in a wooden box and a brewing guide.


## Prompt 10
- Tool: Antigravity AI
- Type: code
- Prompt:
  > Review BRAND.md and README.md constraints. Design an inline SVG logo for 'Mistvale Tea Co.' with viewBox="0 0 260 52". The logo must feature an elegant botanical emblem with tea leaf arcs and mountain silhouette in #1f3d2b, #4f7942 and #d9962b, with refined serif typography for 'Mistvale' and clean tracked subtext 'TEA CO. · DARJEELING'. Also generate a high-DPI raster fallback logo.png.
- Outcome: accepted
- Why: Generated a scalable SVG logo (`images/logo.svg`) and high-resolution PNG (`images/logo.png`) that renders crisp at 38px height as required by BRAND.md Section 10.

---

## Prompt 11
- Tool: Antigravity AI
- Type: code
- Prompt:
  > Audit the existing index.html for bugs, broken logic, and constraint violations:
  > 1. List all business rule failures (R1 to R8).
  > 2. Identify UX anti-patterns, framework dependencies to remove, and missing required page sections.
  > 3. Provide the mathematical corrections for coupon WELCOME10, shipping thresholds, and Indian currency formatting.
- Outcome: accepted
- Why: Uncovered critical subtle bugs: string concatenation in cart quantity (`value + 1`), DOM price parsing reading commas incorrectly, coupon accumulating iteratively and discounting non-eligible gift boxes, `cart.splice(i)` dropping trailing items, missing async debounce on `API.search()`, unhandled promise rejection in `API.checkPincode()`, and expired countdown timer.

---

## Prompt 12
- Tool: Antigravity AI
- Type: code
- Prompt:
  > Rewrite index.html as a single self-contained file with all CSS and JavaScript inline. Follow BRAND.md design rules strictly:
  > - CSS variables: --tea-green (#1f3d2b), --leaf (#4f7942), --cream (#f6f1e7), --parchment (#ebe2cf), --saffron (#d9962b), --ink (#1b1b1b), --error (#b3261e).
  > - Typography: Single Google Fonts link loading Fraunces (headings) and Inter (body) with display=swap.
  > - Page sections in exact order (1 to 10): Announcement strip, Header, Hero, Trust strip, Shop with filters and 2-col/4-col grid, Delivery check, Reviews, FAQ accordion, Inline newsletter, and Footer with legal text.
  > - Implement R1-R8 logic: coupon WELCOME10 (10% off eligible items, capped at ₹150, subtotal >= ₹399, Gifts excluded, case-insensitive), free shipping above ₹499 calculated AFTER discount, sold-out products (stock: 0) always sorted last, pincode check with complete error handling.
  > - Add JSON-LD schema for OnlineStore, Product, and FAQPage.
  > - Add bonus extensions: size selector (100g/250g), wishlist filter with localStorage persistence, and shareable URL query syncing.
- Outcome: modified
- Why: Initial output omitted the required `items` and `coupon` hidden fields in `<form id="checkout-form">`. I manually ensured the exact checkout contract form was preserved and submitted with serialized JSON array `[{"id":101,"qty":2}]`.

---

## Prompt 13
- Tool: Antigravity AI
- Type: code
- Prompt:
  > Write an automated test suite in Node.js to rigorously verify all 8 business rules, constraint compliance (no jQuery, no animate.css, no font-awesome), coupon math edge cases, sold-out sort guarantees, and API pincode error handling.
- Outcome: accepted
- Why: Confirmed that all 8 business rules passed automated verification without breaking any constraints.

---

## Prompt 14
- Tool: Antigravity AI
- Type: code
- Prompt:
  > Please add a "Recently Viewed Teas" extension feature to index.html in pure Vanilla JS and CSS, fully aligned with BRAND.md.
  > - Save viewed product IDs in localStorage (`mv_recently_viewed`), capped at max 4 items with deduplication.
  > - Add a responsive grid section above the footer that stays hidden when history is empty.
  > - Include a helper `getRecentlyViewed(excludeId)` to prevent the currently active product from appearing in its own Quick View modal strip.
  > - Ensure zero external library dependencies and zero modifications to `PRODUCTS` or `API` objects.
- Outcome: accepted
- Why: Implemented a smooth, persistent recent items history that integrates seamlessly with the store's design tokens and cart logic.