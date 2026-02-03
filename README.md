# DMI Portfolio Website (Static HTML/CSS)

This repository contains a clean, professional-looking **static portfolio website** used in **DevOps Micro Internship (DMI)** Week 1 to practice:
- Linux basics
- Nginx hosting
- Deployment proof / ownership
- Production-style checks

✅ Students deploy this website on an Ubuntu VM using Nginx and keep it live for 24 hours.

---

## Who is this for?
- DMI students (beginner → intermediate)
- Anyone learning how to host a static site with Nginx on Linux

---

## What you will build
A portfolio-style website hosted on:
- **Ubuntu VM**
- **Nginx**
- Accessible via: `http://<public-ip>`

---

## Mandatory Ownership Proof (DMI Rule)
Before you deploy, you MUST edit the footer and add your details:

Original:

```html
<p>Crafted with <span>cloud</span> excellence by Pravin Mishra</p>
```

Add this line (example):

```html
<p><strong>Deployed by:</strong> DMI Cohort 2 | Rahul Sharma | Group 4 | Week 1 | 16-01-2026</p>
```

# 📘 Footer Update — README Documentation

## Overview:

This update introduces a custom footer to the portfolio template. The footer displays the project version, deployment date, author name, and a dynamically generated date in DD Mon YYYY format. The goal is to keep the footer informative, consistent, and automatically updated without manual edits.

### Footer Requirement-

The footer must include:

- Project version

- Deployment date

- Author name

- A dynamic date generated at runtime in DD Mon YYYY format

This ensures the footer always reflects the current date whenever the page is loaded.

---

## How the Date Is Generated:

A lightweight JavaScript snippet runs in the browser and:

- Fetches today’s date

- Converts it into the format DD Mon YYYY

- Injects it into the footer using the element with ID today-date

This avoids hard‑coding dates and keeps the footer automatically updated.

---

## Code Snippet (HTML + JavaScript):

### HTML Footer-

```html
<footer>
  <p>
    Pravin Mishra Portfolio v1.0 — Deployed on <span id="deployDate"></span> — By Pradeep Kumar Neelaboyina
  </p>
</footer>
```

### JavaScript (Dynamic Date)-

```html
<script>
  const today = new Date();

  const day = String(today.getDate()).padStart(2, '0');

  const monthNames = ["Jan", "Feb", "Mar", "Apr", "May", "Jun",
                      "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"];
  const month = monthNames[today.getMonth()];

  const year = today.getFullYear();

  document.getElementById("deployDate").textContent = `${day} ${month} ${year}`;
</script>
```

---

## Branch Information:

This update was implemented in the feature branch:

  "feature/footer-v1"

All changes were committed and pushed as part of the footer enhancement task.

---

✅ This proof must be visible in your browser screenshot submission.
