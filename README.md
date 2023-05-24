# Create an offline-first and installable PWA with SvelteKit and workbox-precaching

**[Read Article](https://www.sarcevic.dev/offline-first-installable-pwa-sveltekit-workbox-precaching)**

Slides and Video planned...

TLDR code snippets:

- `npm create svelte@latest my-offline-app`
- extract [app-icons.zip](https://www.sarcevic.dev/offline-first-installable-pwa-sveltekit-workbox-precaching/app-icons.zip) to `/static/`
- create `/static/manifest.json`
  ```json
  {
    "name": "My offline App!",
    "short_name": "Offline App",
    "start_url": "/",
    "display": "standalone",
    "theme_color": "#ff3e00",
    "background_color": "#ffffff",
    "icons": [
      {
        "sizes": "192x192",
        "src": "icon192.png",
        "type": "image/png"
      },
      {
        "sizes": "512x512",
        "src": "icon512.png",
        "type": "image/png"
      }
    ]
  }
  ```
- edit `/src/app.html`
  ```html
  <!-- ... -->
  <head>
    <!-- ... -->
    <link rel="manifest" href="%sveltekit.assets%/manifest.json" />
    <title>My Offline App!</title>
    <link rel="icon" href="%sveltekit.assets%/icon.svg" />
  </head>
  <!-- ... -->
  ```
- `npm install -D workbox-precaching`
- create `/src/service-worker.js`

  ```js
  import { build, files, prerendered, version } from "$service-worker";
  import { precacheAndRoute } from "workbox-precaching";

  const precache_list = [
    "/", // Attention: serves stale index, might not be ideal for your use case.
    ...build,
    ...files,
    ...prerendered,
  ].map((s) => ({
    url: s,
    revision: version,
  }));

  precacheAndRoute(precache_list);
  ```

- edit `/vite.config.js`
  ```js
  // ...
  const config = {
    // ...
    define: {
      "process.env.NODE_ENV": '"production"',
    },
    // ...
  };
  // ...
  ```
- `npm run dev`
  - or `npm run build` and then `npm run preview`
