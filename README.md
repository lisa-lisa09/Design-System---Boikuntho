# Boi Kuntho (বইকুণ্ঠ) Design System — build log

> **13 Nov 2026 — mobile-first correction.** Boi Kuntho is a **mobile app**. All user screens are now 390 × 844 (checked at 360). Earlier desktop screens are archived on page `99.1 Desktop Exploration (Archive)`. See “Mobile correction” below; it supersedes the website-oriented notes that follow.

The design system lives in the Figma file **Boikuntho**
(`https://www.figma.com/design/xs3jtwLAeIJIhuCvcPKzXz/Boikuntho`).
This repository holds only this written summary. All design work is in Figma.

## Page structure (in Figma)

| Page | Status |
|---|---|
| 00 — Cover | New |
| 01.1 Brand / Logo | Existing logo guidelines, renamed only (content untouched) |
| 01.2 Color | Existing colour library, renamed only (64 paint styles reused as the single source of truth) |
| 01.3 Typography | New: 25 text styles (13 EN, Plus Jakarta Sans; 12 BN, Hind Siliguri + Anek Bangla), glyph check, bilingual rules |
| 01.4 Spacing | New: 4/8 scale, radius scale, padding and page margins |
| 01.5 Layout Grid | New: 4 grid styles (Desktop 1440/12, Tablet 768/8, Mobile 390/4, Base 8) |
| 01.6 Elevation | New: 4 elevation effect styles + Focus/Ring |
| 01.7 Iconography | Existing 42 Untitled UI icons + Icon Wrapper; added 25 supplementary icons in the same style, plus size and touch-target guidance |
| 02.1 – 02.20 Components | New: one page per component group, each with A · Documentation, B · Source components, C · Playground |
| 03.1 Wireframes | New: 6 low-fi layouts |
| 03.2 High Fidelity — Buyer | New: Home, Search + filters, Book detail (1440), Mobile home (390) |
| 03.3 High Fidelity — Seller | New: List a book, Seller dashboard, Order status + pre-shipping evidence (1440), Mobile order status (390) |
| 04 — Moodboard / Visual Direction | Existing, renamed only |
| 04.1 Licenses & Attributions | New |
| 99 — Archive | Former empty “Page 2” |

## Component sets

Button, Button/Icon · Input/Text, Input/Prefixed (৳ / +880), Input/Textarea, Input/Select ·
Checkbox, Radio · Search/Bar, Search/Suggestion, Search/Panel, Search/Empty result ·
Avatar, Avatar/Identity · Toggle · Progress/Bar, Progress/Steps, Progress/Spinner, Progress/Dots ·
Chip · Badge, Badge/Condition, Badge/Trust, Badge/Count · App Bar/Desktop, App Bar/Mobile ·
Bottom Nav/Item, Bottom Nav · Tab, Tabs/Underline, Tabs/Segmented · OTP/Digit, OTP/Group ·
Alert, Toast, Dialog/Confirm, Empty State · Selection Card · Stat Card, Listing Row, Activity Row ·
Card/Book · Order Tracker · Upload/Dropzone, Upload/Thumbnail ·
Card/Seller, Card/Local Exchange, Condition Summary, Card/Post.

All components use Auto Layout, the existing paint styles, the new text and effect styles,
and component properties (text, boolean, instance swap). The example screens are composed
from instances of these components.

## Constraints followed

- Free Figma features only. No new variables were created; the existing “Brand colours”
  collection (8) from the logo work was left as it was.
- The logo, the colour library and the moodboard were not modified, apart from page renames.
- The Shilpangon file was only read for its page structure. Nothing in it was changed.
- Every Bangla text run uses Hind Siliguri or Anek Bangla. The ৳ sign inside English text is
  set in Hind Siliguri.
- Trust and payment copy is labelled as a prototype: “Seller Reviewed” is a platform status,
  never “Government Verified”. The 24-hour hold is a proposal, not escrow. The OTP screen
  sends no SMS. Local exchange is in person only, with no intercity flow.

## Outstanding / limitations

- No tablet (768) example screens. Tablet behaviour is documented on the grid and App Bar pages.
- Covers and avatars are placeholders. Add real photos as image fills in Figma.
- Variant masters bind text to properties, so state-specific master text such as
  “Please wait…” shows the property default. Override it per instance.
- Two pre-existing text layers on the Moodboard page and one on the Color page put Bangla in
  Inter or Plus Jakarta Sans. They were left untouched because they are the original work.
- Run a contrast spot-check with real photos and a native-reader review of the Bangla copy
  before the final presentation.

## Mobile correction (13 Nov 2026)

**Reused unchanged:** 64 paint styles, logo components, 67 icons, text, effect and grid styles, and most 02.* components.

**Updated components (mobile refinements, no duplicates):**
- `Card/Book`: new `Layout=Compact` variants (171 px, fill 2-up; 158 px at 360) are now the mobile default.
- `Bottom Nav`: now `Mode=Buyer|Seller`. Seller mode has Dashboard · Listings · Add book · Orders · Account. Items fill the width, so the bar is 360-safe.
- `App Bar/Mobile`: new `Type=Root` for tab roots. `App Bar/Desktop` was renamed "(archived)".
- `Button`: `State=Hover` renamed to `State=Pressed` (touch).
- New: `Mobile/System Bar` (status bar, home indicator), `Mobile/Action Bar` (sticky Purchase / Dual / Single CTA), `Bottom Sheet/Header`.
- `Upload/Thumbnail`: master fixes (cover tag width, no stray caption on the Add tile).

**Docs:** the Cover, 01.5 Layout Grid (new “Mobile app viewport 390 × 844” section), 02.10, 02.11, 02.14 and 02.17 now describe a mobile app.

**Mobile screens (`Mobile 390 / …`, fixed top and bottom bars, content scrolls):**
- Buyer (03.2): Home · Search results · Search · Filter sheet · Search · No results · Book detail · Cart · Checkout · Order placed · Order status · Local exchange request.
- Seller (03.3): Dashboard · List a book · 1 Details · List a book · 2 Photos & delivery · List a book · 2 Error · Listing published · Order · Needs evidence · Order · Ready to ship.
- Wireframes (03.1): 8 low-fi 390 × 844 wireframes.

**Prototype:** flows “Buyer journey — Home → Order status” (23 links), “Local exchange request”, and “Seller journey” (15 links).

**QA:** all 17 mobile screens were cloned at 360 px with no overflow, and every Bangla run is set in Hind Siliguri or Anek Bangla.

**Archived (not deleted):** 6 desktop screens, 6 desktop wireframes, and mobile v1 Home and Buyer order status are on page 99.1.

**Still open:** optional screens (seller profile page, posts/reels feed, wishlist, notifications, account), the actual camera/gallery and bottom-sheet interactions (shown as static states), and real photos for covers and avatars.
