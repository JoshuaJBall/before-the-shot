# before-the-shot

App Store version of the Shoot Planner, built on the "Before The Shot" free/pro model.

This is a **separate repository** from `shoot-planner`. That repo stays untouched on `main` — it's what current The Photographer's Method customers are using via the password gate, and it must keep working exactly as it does today.

This repo is the ground for:
- Free/Pro entitlement architecture (currently a hardcoded `isPro` flag in `index.html` — placeholder until StoreKit is wired in)
- The eventual Capacitor/Xcode wrap for the App Store submission
- No password gate — access is controlled by the Free/Pro split instead

## Free vs Pro (current split, not final)

**Free:** a fixed example plan (Landscape, Golden Hour) showing the full Five Decisions method worked through once — not the user's own shoot. Also free: White Balance, Exposure, viewing Plan History.

**Pro (shows upgrade screen when `isPro = false`):** the six-question planning flow itself (building your own plan), Shooting Mode, Consistency Tracker, Reflection, Shoot Brief, Gear Check, Read the Light, Decision Audit, Edit Checklist, Histogram, Focal Length, Colour Cast, Location Scout, DOF, Shot List, Reciprocity, RAW/JPEG, Print, confirming a Five Decisions answer, editing/duplicating a saved shoot.

The reasoning: letting free users build unlimited real plans with full guidance meant they only needed to learn the method once and never needed Pro again. The fixed example plan still demonstrates the depth of the method, but doesn't teach it against the user's own shoot.

To test locally, change `var isPro = false;` near the top of the Pro-gating block in `index.html` to `true` and reload.

## Deployment

GitHub Pages, served from `main` at `/before-the-shot/`.
