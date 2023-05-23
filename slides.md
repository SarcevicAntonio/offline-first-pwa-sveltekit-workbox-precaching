---
highlighter: shiki
layout: cover
lineNumbers: true
background: https://images.pexels.com/photos/2440078/pexels-photo-2440078.jpeg?cs=srgb&dl=pexels-ian-beckley-2440078.jpg&fm=jpg&w=3604&h=5501
title: Slides
---

# Some Slides...

Antonio Sarcevic - 2023

<img class="hover-right w-40" src="/as.svg" alt="Antonio Sarcevic Logo">

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

- <material-symbols-format-list-bulleted-rounded/> Some Bullet Points
- <material-symbols-code-blocks-outline-rounded/> Some Code

<!--
...
-->

---

# <material-symbols-format-list-bulleted-rounded/> Some Bullet Points

- Lorem ipsum dolor sit amet
- consetetur sadipscing elitr
- sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat
  - sed diam voluptua
- At vero eos et accusam et justo duo dolores et ea rebum.
  - Stet clita kasd gubergren
  - no sea takimata sanctus est Lorem ipsum dolor sit amet
      - Lorem ipsum dolor sit amet
- sed diam nonumy eirmod tempor invidunt
- ut labore et dolore magna aliquyam erat

<!-- prettier-ignore-start -->
<!--
...
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
