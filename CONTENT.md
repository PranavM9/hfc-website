# HFC Website — Content Guide

## Hero Section

**File:** `layouts/partials/hero.html`

### What It Is

Full-screen video background. First thing visitors see. Contains the club title, slogan, and a scroll indicator.

---

### Editable Fields

| Field | Where | Notes |
|---|---|---|
| Title | `hero.html` | Line with `<h1 class="hero__title">` |
| Slogan | `hero.html` | Line with `<p class="hero__slogan">` |
| Video | `static/video/hero.mp4` | Drop file here, no code change needed |

---

### Changing the Title or Slogan

Open `layouts/partials/hero.html` and find:

```html
<h1 class="hero__title">HUSKY FLYING CLUB</h1>
<p class="hero__slogan">Where Huskies Take Flight</p>
```

Edit the text between the tags. Do not touch the class names.

---

### Swapping the Video

1. Name your file `hero.mp4`
2. Drop it into `static/video/`
3. Open `layouts/partials/hero.html` and find:

```html
<source src="https://videos.pexels.com/..." type="video/mp4">
```

Replace the `src` value with `/video/hero.mp4`

```html
<source src="/video/hero.mp4" type="video/mp4">
```

Done. No other changes needed.

---

### Adding a Poster Image (Fallback)

Shown while the video loads or on slow connections.

1. Name your file `hero-poster.jpg`
2. Drop it into `static/images/`
3. The `poster` attribute in `hero.html` already points to `/images/hero-poster.jpg` — no code change needed.