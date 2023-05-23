---
highlighter: shiki
layout: cover
lineNumbers: true
background: https://images.pexels.com/photos/3387174/pexels-photo-3387174.jpeg?cs=srgb&dl=pexels-vlad-che%C8%9Ban-3387174.jpg&fm=jpg&w=5133&h=3422
title: Slides
---

# Create an offline-first and installable Web App

## with <logos-svelte-icon/> SvelteKit and <file-icons-workbox/> workbox-precaching

Antonio Sarcevic - 2023

<img class="hover-right w-40" src="/icon.svg" alt="Offline Svelte App Logo">

<!-- prettier-ignore-start -->
<!--
...
-->
---
layout: image-right
image: https://images.pexels.com/photos/1840142/pexels-photo-1840142.jpeg?cs=srgb&dl=pexels-vitor-almeida-1840142.jpg&fm=jpg&w=3024&h=4032
---
<!-- prettier-ignore-end -->

# <material-symbols-view-agenda/> Overview

- <simple-icons-pwa/> What is PWA?
- <material-symbols-emoji-symbols-rounded/> App Icons
- <material-symbols-document-scanner-rounded/> Web App Manifest
- <material-symbols-settings-suggest-outline-rounded/> Service Worker

<!--
...
-->

---

# <simple-icons-pwa/> What is PWA?

- PWA stands for progressive web apps
- browser features
  - <material-symbols-document-scanner-rounded/> Web App Manifest
  - <material-symbols-settings-suggest-outline-rounded/> Service Worker
- native app-like behaviour
  - <material-symbols-install-mobile-rounded/> installable as "standalone app" on operating systems
  - <material-symbols-offline-pin-rounded/> offline support / offline-first

<!-- prettier-ignore-start -->
<!--
- navigator apis
- and even more
  - push notifications
  - shortcuts / quick actions
  - protocol handlers
  - app icon badging
-->
---
layout: image-right
image: https://images.pexels.com/photos/1830667/pexels-photo-1830667.jpeg?cs=srgb&dl=pexels-akshay-praneeth-1830667.jpg&fm=jpg&w=4000&h=6000
---
<!-- prettier-ignore-end -->

# <material-symbols-format-list-bulleted-rounded/> Some Bullet Points with image

- Lorem ipsum dolor sit amet
- consetetur sadipscing elitr
- sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat
  - sed diam voluptua
- At vero eos et accusam et justo duo dolores et ea rebum.
  - Stet clita kasd gubergren
  - no sea takimata sanctus est Lorem ipsum dolor sit amet
    - Lorem ipsum dolor sit amet

<!--
...
-->

---

# <material-symbols-code-blocks-outline-rounded/> Some Code

## [`TicTacToeParameters.svelte`](https://git.fh-muenster.de/swa1/coding-challenge/platform/-/blob/987a29b89ea68bdb56037922bf41bf73560ca667/FrontEnd/src/lib/games/TicTacToeParameters.svelte)

```html{all|4-13|15-19|23-47}
<script>
  import { onMount } from "svelte";

  // 🔢 Standardwerte ✅
  let defaults = {
    parameters: {
      gameBoardSize: {
        rows: 3,
        columns: 3,
        winningLength: 3,
      },
    },
  };

  // ✏️ `matchConfig` mutieren ✅
  export let matchConfig;
  onMount(() => {
    matchConfig = { ...matchConfig, ...defaults };
  });
</script>

{#if matchConfig.parameters && matchConfig.parameters.gameBoardSize}
<!-- 📝 Formularelemente ✅ -->
<label>
  # of rows
  <input
    type="number"
    min="1"
    bind:value="{matchConfig.parameters.gameBoardSize.rows}"
  />
</label>
<label>
  # of columns
  <input
    type="number"
    min="1"
    bind:value="{matchConfig.parameters.gameBoardSize.columns}"
  />
</label>
<label>
  Length of connected tiles to win
  <input
    type="number"
    min="1"
    bind:value="{matchConfig.parameters.gameBoardSize.winningLength}"
  />
</label>
{/if}
```

<!--
...
-->

---

# <material-symbols-code-blocks-outline-rounded/> Some Code

- Lorem ipsum dolor sit amet
- consetetur sadipscing elitr

```json
{} // erlaubt valides JSON jeder Art
```

```json
{ "type": "string" } // erlaubt JSON vom Typ String (z.B. "Hello JSON Schema")
```

```json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "type": "object",
  "properties": {
    "someKey": {
      "type": "string"
    }
  }
} // erlaubt ein JSON Objekt mit someKey und Wert vom Typ String (z.B. { someKey: "Hello JSON Schema" })
```

<!-- prettier-ignore-start -->
<!--
- Game Parameters als beschreibung eines JSON Objekts
- JSON Schema als Spezifikation von JSON Dokumenten
  - kann z.B. Objekte Beschreiben
  - wird in der Regel zum validieren von JSON Dokumenten genutzt
 -->

---
layout: cover
background: https://images.pexels.com/photos/16929691/pexels-photo-16929691.jpeg?cs=srgb&dl=pexels-brayan-berrospi-silvestre-16929691.jpg&fm=jpg&w=2812&h=3515
---
<!-- prettier-ignore-end -->

# Thank you for your time

## I hope it was worthwhile ✌️

Antonio Sarcevic - 2023

<img class="hover-right w-25" src="/as.svg" alt="Antonio Sarcevic Logo">
