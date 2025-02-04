# [reveal.js-mermaid-plugin](https://github.com/baldir-fr/reveal.js-mermaid-plugin)

A Mermaid plugin for reveal.js.

## Install

```shell
npm install https://github.com/baldir-fr/reveal.js-mermaid-plugin
```

## Usage

```html
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/reveal.js@4.3.1/dist/reset.css"
/>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/reveal.js@4.3.1/dist/reveal.css"
/>
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/reveal.js@4.3.1/dist/theme/black.css"
  id="theme"
/>

<div class="reveal">
  <div class="slides">
    <section>
      <h3>Flowchart</h3>
      <div class="mermaid">
        <pre>
          %%{init: {'theme': 'dark', 'themeVariables': { 'darkMode': true }}}%%
          flowchart TD
            A[Start] --> B{Is it?};
            B -- Yes --> C[OK];
            C --> D[Rethink];
            D --> B;
            B -- No ----> E[End];
        </pre>
      </div>
    </section>
  </div>
</div>

<script src="https://cdn.jsdelivr.net/npm/reveal.js@4.3.1/dist/reveal.js"></script>
<script src="https://cdn.jsdelivr.net/gh/baldir-fr/reveal.js-mermaid-plugin/plugin/mermaid/mermaid.js"></script>
<script>
  Reveal.initialize({
    controls: true,
    progress: true,
    center: true,
    hash: true,

    plugins: [RevealMermaid],
  });
</script>
```
