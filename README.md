# PIVOT — Gym Booking Demo | VYB

**A responsive gym website concept designed and developed by VYB.**  
**Portfolio demo · Fictional gym · English / Español**

PIVOT is an example of a premium gym/personal training website. It presents strength training, personal coaching, services, illustrative prices, photographs, opening hours and a **Booking-ready user interface**.

> **Important:** PIVOT is a **fictional business** created to demonstrate VYB’s work. The photographs, schedules and prices are examples. **Online bookings are not active in this public demo**, and no reservation will be created.

## Features

| Area | What's included |
| --- | --- |
| **Gym Booking design** | Prominent booking calls to action and a booking interface ready for a future dedicated scheduling link. |
| **No live booking URL** | The previous shared test calendar was removed. Clicking a booking CTA displays an honest configuration notice, without redirecting to another business. |
| **Responsive layouts** | Desktop and mobile presentation, mobile navigation and readable content. |
| **Bilingual** | English / Spanish language toggle. |
| **Training programs** | Personal training, strength and other example services, with illustrative prices. |
| **Gallery** | Training photos with an interactive image viewer. |
| **Easy publishing** | Static HTML, CSS and JavaScript; no build or backend required to publish this package. |

## Live preview

The live URL will be available in **GitHub → Repository → Settings → Pages** after publishing. No deployment URL has been invented or hard-coded in this README.

### Booking status

This is the **Booking layout**, not a connected appointment service. The `booking.url` value in [`config.js`](config.js) is deliberately empty:

```js
"booking": {
  "url": "",
  "mode": "modal"
}
```

A click on any booking button shows a clear message: online bookings are not connected yet. This is intentional so the Gym demo never sends visitors to VYB's Obsidian barbershop calendar or another unrelated account.

When a real gym authorizes its own booking account, replace the empty URL with its verified HTTPS booking URL and test it. In `modal` mode, the existing app only embeds official HTTPS Setmore subdomains; for other booking services, switch to `external` mode and use an approved HTTPS URL. Do not add credentials or customer data to this public file. **The active booking flow and actual appointment confirmations have not been tested for this disconnected demo.**

## Repository structure

```text
.
├── index.html       # Public website (GitHub Pages entry)
├── styles.css       # Responsive styling
├── app.js           # Navigation, translations, gallery and booking actions
├── config.js        # Public sample text, styles, services and booking setting
├── assets/          # Local example photos
├── favicon.svg      # Demo icon
├── .nojekyll        # GitHub Pages compatibility
├── .gitignore       # Local-only files exclusions
└── README.md        # GitHub repository introduction
```

Only the **Gym Booking** output is included. The original VYB template generator and development tools remain in the source project, not in this public-site package.

## Publish on GitHub Pages

1. Create a new repository in your GitHub account (for example, `VYB-Gym-Booking`).
2. Download and **extract** this ZIP; upload the **files inside**, directly into the repository root (do not upload the ZIP itself or an enclosing folder).
3. Commit the upload to the default branch, usually `main`.
4. In **Settings → Pages → Build and deployment**, choose **Deploy from a branch**.
5. Select `main` and **`/(root)`**, then Save.
6. Once GitHub reports that deployment is complete, use the **Visit site** link to open the demo.
7. Test desktop and mobile views, switch both languages, browse services/gallery and click all Booking buttons. They should show the unavailable notice rather than open a calendar.

You may need sufficient permissions in the repository to enable Pages. The static site works without Node.js, packages, a database or server-side deployment.

## Run locally

From the extracted directory:

```bash
python -m http.server 8080
```

Then visit `http://localhost:8080/`. On Windows you can use `py -m http.server 8080` if Python is installed.

## Customizing for a real gym

All demo-specific values are in [`config.js`](config.js), including:

- `business`: gym name and demo notice.
- `images`: example local assets and their labels.
- `businessDetails`: illustrative address and opening hours.
- `contact`: currently empty; add only published, authorized business contact information.
- `services`: names, duration and prices.
- `booking.url`: a **dedicated booking account for this gym**, once it exists.
- `seo`: title, description and future canonical URL.

The source project uses a generator (`tools/build.mjs`), so permanent modifications to a reusable template should be made in the original sources and rebuilt. This distribution is already generated for hosting.

Do not publish passwords, private API keys or personal customer data. Check rights to sample photography and fonts before reuse for commercial customers. This fictional demo includes `noindex, nofollow` to avoid its appearance as a real local gym in search engines; review SEO settings for a legitimate client deployment.

---

## Español — Sobre la demostración

**PIVOT** es una demo de VYB que presenta cómo puede verse un sitio web **Booking para gimnasios**. Tiene secciones de entrenamientos, servicios, galería, horarios de ejemplo, diseño adaptable a celular y selector de idiomas.

**Las reservas NO están habilitadas.** Se eliminó el enlace de Setmore de la barbería Obsidian. Al tocar cualquier botón de reserva, la página muestra un aviso y no dirige al visitante a otro negocio. Cuando exista un cliente real, se podrá conectar su calendario de reservas propio.

Para publicarlo, subí **el contenido del ZIP descomprimido directamente a la raíz del repositorio**; entrá a **Settings → Pages**, seleccioná la rama `main` y la carpeta `/(root)`.

El sitio es estático: no necesita backend, compilación ni instalar dependencias. Las imágenes, servicios, precios y horarios son ilustrativos, no corresponden a un gimnasio real.

*VYB · Web Design & Development · 2026*
