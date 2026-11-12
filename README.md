# Boi Kuntho (বইকুণ্ঠ) Design System — build log

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
