<div align="center">

# 📸 LensCraft Photography

**A multi-page photography portfolio — built in pure HTML & CSS. No JavaScript. No frameworks.**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![Pages](https://img.shields.io/badge/Pages-11-C9A24B?style=flat-square)

[🔗 Live Demo](https://zahid60.github.io/LensCraft-Photography-Website/)

<img src="./LensCraft-Photography-Website Images.png"/>

</div>

---

## About

LensCraft is a portfolio for a Kyoto-based photography studio, built around six specialities — Nature, Portrait, Wedding, Street, Travel, and Wildlife. One deliberate constraint shaped all of it: everything had to work in pure HTML and CSS, including the things people normally reach for JavaScript to build, like the image lightbox.
 
The goal was simple to state and harder to build: a professional, multi-page portfolio a real studio could actually use, with a clear path from browsing the work to booking a session, and full responsiveness across every device. **Eleven pages. Fifty-six-plus photographs. Six categories. Not a single line of JavaScript** — the numbers are proof the constraint held.

## ✨ Features

- **11 static pages** — Home, Gallery, Services, Blog, Contact, and 6 category galleries
- **CSS-only lightbox** — full-screen photo viewer with prev/next/close, built with the `:target` pseudo-class instead of JavaScript
- **Responsive layout** — CSS Grid & Flexbox, with breakpoints at 992 / 768 / 480px
- **One shared design system** — every color, shadow, and radius is a CSS custom property in `:root`, so the whole site re-themes from one place
- **Pricing plans, service icons, blog cards, client reviews** — all hand-built, hover effects included, all pure CSS
- **Native HTML `<marquee>`** promo banner under the header
- **Custom SVG logo + generated favicon** (16×16, 32×32, Apple touch icon)

## 🛠️ Built With

`HTML5` · `CSS3` (Custom Properties · Grid · Flexbox · `:target`) · `Fraunces` + `Poppins` (Google Fonts)

No JS. No frameworks. No build step.

## 📁 Project Structure

```
├── index.html              # Home
├── gallery.html             # Links to all 6 category pages
├── services.html            # Services + pricing plans
├── blog.html                 # Blog post grid
├── contact.html            # Booking form
├── nature.html               │
├── portrait.html             │
├── wedding.html               ├─ Category galleries (CSS-only lightbox)
├── street.html                │
├── travel.html                │
├── wildlife.html             │
├── favicon.ico / favicon-16x16.png / favicon-32x32.png / apple-touch-icon.png
└── assets/
    ├── css/
    │   └── style.css        # Entire site's styling — one shared design system
    └── img/
        ├── brand/           # Logo mark, logo lockup
        ├── cover/           # Homepage hero photo
        ├── featured/        # Thumbnails used on Home & Gallery
        └── nature/ portrait/ wedding/ street/ travel/ wildlife/
                              # Full photo sets per category
```

## 🪄 How the CSS-Only Lightbox Works

Every gallery photo is an anchor pointing at an id; the lightbox overlay uses `:target` to reveal itself when the URL hash matches — no JavaScript anywhere:

```html
<a class="frame" href="#photo-1">
  <img src="photo-1.jpg">
</a>

<div class="lightbox-css" id="photo-1">
  <img src="photo-1.jpg">
  <a href="#" class="lightbox-close">&times;</a>
</div>
```

```css
.lightbox-css        { display: none; }
.lightbox-css:target { display: flex; }   /* URL hash opens the photo */
```

## 📄 License

This project was built for academic purposes. Photography used is for demonstration only — replace with licensed or original images before any real-world/commercial use.
