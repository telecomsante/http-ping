# \<http-ping\>

[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/telecomsante/http-ping)

Ping http(s) url

A simple no GUI component to ping an url. The component use the fetch API, so use it with recent browser.

By default, the component ping google.com

> Nota ; fetch polyfill doesn't work due to CORS problems.

tested on :

 - chrome
 - firefox
 - safary TP ( doesn't work on safari )
 - opera
 - Edge

## Quick example

<!--
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="http-ping.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<http-ping interval="2000"></http-ping>
<div class="status"></div>
<div class="delay"></div>
<script>
const ping = document.querySelector('http-ping')
ping.addEventListener('ping-status', evt => {
  document.querySelector('.status').innerHTML = evt.detail.status ? "connected":"not connected";
});
ping.addEventListener('ping-delay', evt => {
  document.querySelector('.delay').innerHTML = evt.detail.delay ? `${evt.detail.delay} ms`:'-';
})
</script>
```

The component is licensed under the [ISC License](LICENSE.md)

Demo and doc are available on https://telecomsante.github.io/http-ping/
