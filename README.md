# Cronitor — Developer Monitoring Landing Page

A pixel-perfect, responsive replica of the developer-centric landing page for **[Cronitor](https://cronitor.io)**. Built with semantic HTML5, modern Tailwind CSS, and vanilla JavaScript in an ultra-clean, zero-dependency single-file architecture.

---

## 📖 Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Architecture & Design Details](#architecture--design-details)
  - [Typography & Visual Language](#typography--visual-language)
  - [UI Mockups & Interactive Elements](#ui-mockups--interactive-elements)
- [Customization Guide](#customization-guide)
- [Browser Compatibility](#browser-compatibility)
- [License & Disclaimer](#license--disclaimer)

---

## 🚀 Overview

Cronitor is an established telemetry and monitoring tool specifically engineered for developers, cron jobs, background workers, websites, APIs, and microservices. 

This project recreates its signature landing page with high fidelity, emphasizing:
- Monospaced, terminal-inspired developer aesthetics (`Space Mono`).
- Modern clean typography for reading ergonomics (`Inter`).
- Realistic telemetry dashboards showing real-time heartbeat statuses, latency pills, and multi-region availability checks.
- Zero external build tool requirements — ready to deploy or integrate immediately.

---

## ✨ Key Features

1. **Pixel-Perfect Hero Section**
   - Developer-focused title copy, CTA buttons, and reassurance badges.
   - Realistic macOS-style dashboard mockup featuring live status indicators, uptime health blocks, response latency timings, and SSL cert tracking.

2. **Social Proof & Client Badges**
   - Grayscale and high-contrast logos representing industry engineering teams (eBay, DigitalOcean, Reddit, Postman, Sentry, Loom).

3. **5 Detailed Feature Showcases**
   - **Cron Job & Agent Monitoring:** Execution timeline visual and zero-code CLI wrapper code block.
   - **Uptime, Performance, and SSL:** Multi-region edge node latency breakdown and SSL expiry tracker.
   - **Heartbeat Telemetry:** Visual uptime block grid with ping indicators and curl command snippet.
   - **Hosted Status Pages:** Live preview of a clean, hosted incident status dashboard.
   - **Website Performance Analytics:** Vector-rendered p95/p99 latency distribution graph.

4. **Integration Ecosystem Grid**
   - Coverage grid highlighting SDKs for Node.js, Python, Go, Ruby, PHP, Java, Bash CLI, AWS Lambda, and Kubernetes.

5. **Customer Proof & Case Studies**
   - Testimonial pull-quote from infrastructure leadership.
   - Case study cards for enterprise users (Slate, Great Waves).

6. **Fully Responsive Layout**
   - Responsive breakpoints (`sm`, `md`, `lg`) tuned for phones, tablets, and widescreen desktop displays.
   - Built-in collapsible mobile navigation drawer.

---

## 🛠️ Tech Stack

- **HTML5:** Semantic markup structure with full accessibility considerations.
- **Tailwind CSS (CDN v3):** Utility-first styling with custom extended theme configuration.
- **Google Fonts:**
  - `Space Mono` (400, 700) — Headings, code snippets, telemetry chips, and status tags.
  - `Inter` (400, 500, 600, 700) — High-legibility body copy and navigation links.
- **JavaScript (Vanilla):** Lightweight script for toggling the mobile navigation menu.

---

## 📁 Project Structure

The entire project is structured into a single file for maximum portability and zero setup overhead:

```text
├── index.html          # Complete HTML document including Tailwind config, SVG graphics, and scripts
└── README.md           # Comprehensive project documentation
```

---

## ⚡ Getting Started

### Prerequisites

No build tools (such as Node.js, npm, or webpack) are required. All styling and font assets load via high-speed CDNs.

### Running the Website

#### Method 1: Direct File Launch
Double-click `index.html` or drag-and-drop it into any modern web browser (Chrome, Firefox, Safari, Edge, Brave).

#### Method 2: Local Development Server (Recommended)
Using Python:
```bash
# Python 3
python -m http.server 3000
```
Then navigate to `http://localhost:3000` in your browser.

Using Node.js (`npx`):
```bash
npx serve .
```

Using VS Code:
- Install the **Live Server** extension.
- Right-click `index.html` and select **"Open with Live Server"**.

---

## 🎨 Architecture & Design Details

### Typography & Visual Language

The design relies heavily on a contrast between clean modern sans-serif body text and precise monospaced accents:

```html
<!-- Font configuration declared in Tailwind configuration -->
<script>
  tailwind.config = {
    theme: {
      extend: {
        fontFamily: {
          mono: ['"Space Mono"', 'monospace'],
          sans: ['"Inter"', 'sans-serif'],
        }
      }
    }
  }
</script>
```

### UI Mockups & Interactive Elements

- **Uptime Bars:** Built using consecutive flexbox elements with variable green (`#10B981`) and warning amber (`#F59E0B`) backgrounds.
- **Terminal Snippets:** Styled dark blocks with high-contrast colored shell commands (`curl`, `cronitor exec`).
- **Telemetry Indicators:** Pulsing CSS animation (`animate-pulse`, `animate-ping`) for active status indicators.

---

## 🔧 Customization Guide

### 1. Changing Brand Colors
Update the `colors` property inside the inline Tailwind script in `<head>`:
```javascript
colors: {
  brand: {
    cream: '#FAFAF7',
    dark: '#111827',
    accent: '#2563EB',
    green: '#10B981'
  }
}
```

### 2. Adding / Modifying Monitor Rows
In the hero dashboard section, duplicate or edit the monitor rows inside the table container:
```html
<div class="px-4 py-3 flex items-center justify-between min-w-[580px] hover:bg-gray-50 transition">
  <div class="flex items-center gap-3 w-48">
    <span class="w-2.5 h-2.5 rounded-full bg-emerald-500"></span>
    <div>
      <div class="font-mono font-bold text-gray-900 text-xs">your-job-name</div>
      <div class="text-[10px] text-gray-400">Schedule description</div>
    </div>
  </div>
  <!-- Add custom uptime blocks here -->
</div>
```

---

## 🌐 Browser Compatibility

Tested and fully supported on:
- Google Chrome (latest)
- Mozilla Firefox (latest)
- Apple Safari (macOS & iOS)
- Microsoft Edge (latest)
- Brave & Chromium-based browsers

---

## 📄 License & Disclaimer

- **Disclaimer:** This project is an educational and portfolio recreation of the Cronitor landing page design. All trademarks, logos, and brand names belong to their respective owners (Cronitor, Inc.).
- **License:** Open-source and available under the [MIT License](https://opensource.org/licenses/MIT).
