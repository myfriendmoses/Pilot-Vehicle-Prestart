# GPS - Daily Vehicle Pre-Start Application

A streamlined, mobile-first Progressive Web Application (PWA) designed for **Goodwin Piloting Services** to complete and export daily vehicle compliance safety checks. Built completely in a single file with native web standards, this app ensures offline-ready usage on-site and easy data reporting via clipboard or email.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![PWA](https://img.shields.io/badge/PWA-5A0FC8?style=flat-square&logo=progressive-web-apps&logoColor=white)

---

## 🚀 Key Features

* **PWA Gate Shield:** Restricts access on mobile web browsers until the application is added/installed directly to the device's home screen. Features tailored guides for both iOS (Safari) and Android (Chrome).
* **Offline Capability:** Built-in Service Worker logic allows the checklist to load seamlessly even when operating outside cellular network coverage zones.
* **Persistent Local Storage:** Form fields and checklist data automatically save to `localStorage` on every change. Never lose field entries due to app closures or accidental tab reloads.
* **Monospaced Summary Matrix:** Dynamically formats inspection details into a clean, alignment-padded plaintext summary matrix ready for immediate export.
* **Export Integrations:**
    * **Copy Summary:** Quick clipboard injection via a safe overlay layer fallback.
    * **Send via Email:** Automagically builds formatted `mailto:` links injecting standard Subject and structured summary logs directly into your default email client.

---

## 🛠️ Tech Stack & Architecture

This application architecture follows a **Single-File App (SFA)** layout to maximize transportability and zero-config local file loading capabilities:

* **Markup:** Structural semantic HTML5 with custom mobile viewport tuning configurations.
* **Styling:** Modern, responsive CSS Variable-driven architecture mimicking standard UI frameworks (Tailwind token aesthetics) using native grids and flexboxes.
* **Logic Engine:** Vanilla ECMAScript 6 JavaScript handling state machines, layout rendering, clipboard fallback API management, and `localStorage` JSON parsing.

---

## 📋 Pre-Start Checklist Parameters

The application captures essential regulatory operational metrics including:

* **Fleet Details:** Rego, Driver/Inspector, Current Odometer.
* **Compliance Trackers:** Service Interval (KM), RUC Balance (KM), WOF Expiry Date, Registration Due Date.
* **System Status Controls:** Segmented Pass/Fail/NA toggles monitoring:
    * Engine Oil & Fluid Levels
    * Tyre Tread & Air Pressures
    * Illumination Systems (Lights & Indicators)
    * Glass, Wipers & Fluid Washers
    * Brakes & Secondary Handbrake Action
    * Seatbelts & Cabin Restraints
    * Specialist Pilot Safety Equipment (Signs & Warning Lights)

---

## 📦 How to Deploy

Because this app utilizes a standard, standalone infrastructure layout, deployment requires zero compilation steps:

### Option A: Static Hosting (Recommended)
1. Drop `index.html` and your company asset `logo.png` into any public file store or static server container (e.g., GitHub Pages, Cloudflare Pages, Vercel, or Netlify).
2. Point your corporate mobile device browsers to the deployment URL.

### Option B: Local Server Testing
If testing on a local desktop workspace:
```bash
# Run a quick local static node server instance
npx serve .
# Or using python
python -m http.server 8080
