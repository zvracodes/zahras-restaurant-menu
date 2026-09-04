# Zahra's Restaurant — Multi-Color Menu Website 🍽️

A restaurant menu website that changes its entire color theme using **pure CSS Variables and HTML only — no JavaScript**.

## 🔗 Live Demo
[View Live Website](https://zvracodes.github.io/zahras-restaurant-menu/)

## ✨ Features

- 4 switchable color themes: **Classic Din**, **Tandoor Raat**, **Iftar Special**, and **Chai Corner**
- Instant theme switching — no page reload
- Fully built with HTML & CSS — **zero JavaScript**
- Responsive menu layout with categorized dishes (Starters, BBQ & Tandoor, Karahi & Biryani, Drinks & Desserts)

## 🛠️ Built With

- HTML5
- CSS3 — Custom Properties (CSS Variables)
- The `:has()` CSS selector

## 💡 How the Theme Switching Works

Instead of using JavaScript, this project uses a combination of:

1. **CSS Variables** (`:root { --primary: ...; }`) — a single source of truth for all colors used across the site
2. **Hidden radio inputs** — one for each theme, acting as the "current state"
3. **The `:has()` selector** — lets the page detect which radio is checked and override the root variables accordingly

```css
:root {
  --bg: #faf3e8;
  --primary: #8b1e3f;
}

body:has(#theme-raat:checked) {
  --bg: #17110d;
  --primary: #e8632c;
}
```

Because every element on the page reads its color from `var(--bg)`, `var(--primary)`, etc., the entire site repaints instantly when a different theme is selected — with no JavaScript involved.

##  What I Learned

This was a hands-on project to practice:
- Defining and reusing CSS custom properties
- Managing color consistency across a full page using variables
- Using `:has()` as a JavaScript-free way to build interactive, stateful UI
- CSS specificity and how nested selectors can unintentionally affect unrelated elements
- Basic Flexbox layout (`justify-content`, `align-items`)

## 🚀 Next Steps

- Add JavaScript + `localStorage` so the selected theme persists after refresh
- Make the layout fully responsive for mobile devices

---

Built by Zahra as a learning project while studying HTML & CSS.

