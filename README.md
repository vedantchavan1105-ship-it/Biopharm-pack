# BioPharm-Pack V34 — Owner Analytics + Research History + Original Logo

## What is new
- Owner/Admin dashboard for non-sensitive research activity history.
- Cross-device logging when the website is served by the included Node.js server.
- LocalStorage fallback for offline/local-file demonstrations.
- Owner password is validated by the server; activity logs never store the password.
- CSV export for project documentation.
- No IP-address collection by the included server.
- Activity consent is included in the research-workspace acknowledgement.

## Run the real cross-device version
1. Install Node.js 18+ on the computer/server that will host BioPharm-Pack.
2. In this folder, set an owner password. Example on Windows PowerShell:
   `$env:ADMIN_PASSWORD="your-strong-password"`
   On macOS/Linux: `export ADMIN_PASSWORD="your-strong-password"`
3. Start: `node server.js`
4. Open `http://localhost:3000` (or the server's LAN/public URL from another device).
5. Choose Research Workspace → Owner / Admin.
6. Enter the configured owner password.

The server stores activity in `data/activity.json`. Back it up and protect the server. Do not expose the default password; the server refuses the placeholder password.

## Demo/offline mode
If `index.html` is opened directly as a file/content URL, the activity dashboard falls back to browser-local demo history. The demo owner password is `BPP-ADMIN-DEMO`. This mode cannot collect activity from other people's devices because there is no shared server.

## Privacy
The prototype is designed to record only explicit non-sensitive research events (e.g., selected drug record, feature opened, packaging action). It does not intentionally record patient data, passwords or IP addresses. For public deployment, publish a final privacy notice, define retention/deletion, secure the admin account, use HTTPS, and obtain any institutional consent required for your study/demo.


V33 LOGO INTEGRATION FIX
- Logo and icon are embedded directly into index.html as data URIs, so local/offline Android content:// opening does not depend on sibling image paths.
- Favicon embedded.
- Existing external real-product reference images remain unchanged and retain their offline fallback behavior.
- Existing V31 server/admin/research-history features are preserved.


## V34 permanent reliability fixes
- Fixed admin login comparison for passwords of different lengths (no server exception).
- Removed reliance on the hard-coded demo password path; owner login requires ADMIN_PASSWORD configuration.
- Hardened static-file path resolution against traversal.
- Added server version/status reporting and nosniff response header.
- Existing website UI, research workflow, local data and features are preserved.


## V38 expanded drug library
- Added a searchable drug research index with 200+ commonly encountered medicines and dosage forms.
- Search works by generic name, therapeutic class, and common dosage form.
- Expanded records are navigation/research aids and do not reproduce protected pharmacopoeial monograph text or acceptance limits.
- Current monograph/regulatory status must be verified through the official Indian Pharmacopoeia Online route.
- Existing website layout, server, logo, packaging workflow, costing and validation logic are preserved.


## V40 — 3D Concept Studio
- Reworked only the 3D Concept view into an interactive research visualization studio.
- Added realistic-looking CSS 3D packaging models for tablet, capsule, syrup, powder/sachet, oral film, injection, oral suspension, cream/gel, eye drops, inhaler, suppository, and transdermal patch.
- Added front, side, back and top view controls.
- Added exploded-view and 360-degree preview controls.
- Added formulation gallery with one-click selection.
- Existing drug library, logo, dashboard, navigation, packaging/cost, validation and other workflows are preserved.
- Visuals are explicitly labeled as research concepts and do not claim regulatory or laboratory validation.


## V40 3D reliability update
- Added pointer/touch drag rotation for the 3D concept viewer.
- Added mouse-wheel/touchpad zoom with bounded scale.
- Reworked reset behavior to restore angle, zoom and exploded state.
- Added actual visual separation for exploded-view components where the concept contains multiple components.
- Kept the rest of the application unchanged.
- 3D visuals remain research/concept visualizations and are not regulatory, stability, compatibility, sterility or manufacturing evidence.

## V42 public-site alignment update
- Improved responsive alignment for Home / About / Privacy / Terms / Support navigation.
- Public document pages now remain centered and contained on desktop, tablet and mobile widths.
- Expanded Privacy Policy with data handling, browser storage, optional server activity, sensitive-data guidance, external sources, and retention/deletion guidance.
- Expanded Terms & Conditions with permitted use, verification duty, no-certification language, illustrative concept limitations, user content, intellectual property, availability/changes, and limitation-of-reliance guidance.
- Added project support contact: vedantchavan1117@gmail.com.
- Existing research workspace and 3D Concept functionality preserved.
