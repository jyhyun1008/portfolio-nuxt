<template>
  <div id="app">
    <NuxtLayout>
      <div id="nav">
          <div id="logo"><a href="/">Hyun Jaeyeon</a></div>
          <div id="nav-list">
            <div class="nav-item"><a href="#content0">About</a></div>
            <div class="nav-item"><a href="#content1">Values</a></div>
            <div class="nav-item"><a href="#content2">Items</a></div>
            <div class="nav-item"><a href="#content3">Contact</a></div>
          </div>
        </div>
        <div id="nav-mobile" style="display: none;">
          <div id="logo-mobile"><a href="/">Hyun Jaeyeon</a></div>
        </div>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>
<style>

@font-face {
    font-family: 'IBMPlexSansKR';
    src: url('https://fastly.jsdelivr.net/gh/projectnoonnu/noonfonts_20-07@1.0/IBMPlexSansKR-Regular.woff') format('woff');
    font-weight: 400;
    font-style: normal;
}

@font-face {
    font-family: 'IBMPlexSansKR';
    src: url('https://fastly.jsdelivr.net/gh/projectnoonnu/noonfonts_20-07@1.0/IBMPlexSansKR-Bold.woff') format('woff');
    font-weight: 700;
    font-style: normal;
}

html {
    scroll-behavior: smooth;
    scroll-timeline: --circleTimeline y;
    /* Firefox supports the older "vertical" syntax */
    scroll-timeline: --circleTimeline vertical;
    overflow-y: scroll;
}

.snap-area {
  scroll-snap-type: y mandatory;
}

:root {
  --accent: #ff9899;
  --accent-light: #ffddcc;
  --fg: #60606d;
  --border: #d7d7de;
  --bg: #f8f8fb;
}

body {
  font-family: 'IBMPlexSansKR';
  margin: 0;
  overflow-x: hidden;
  color: var(--fg);
}

div {
  box-sizing: border-box;
}

@media (max-width: 700px) {
    #nav {    
        display: none !important;
    }
    #nav-mobile {
      display: flex !important;
    }
}

#nav, #nav-mobile {
  position:fixed;
  top: 0;
  left: 0;
  z-index: 9999;
  width: 100vw;
  height: 50px;
  background-color: white;
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-bottom: var(--border) 1px solid;
  box-shadow: 0 5px 5px #00000012;
}

#nav-list, #nav-list-mobile {
  display: flex;
  align-items: center;
}

#logo, #logo-mobile {
  font-weight: 700;
  padding: 0 20px;
  font-size: 1.2em;
  color: var(--accent);
}

#nav a, #nav-mobile a {
  color: inherit;
  text-decoration: none;
}

.nav-item {
  padding: 0 20px;
}

li {
  line-height: 1.8;
}

#nuxt-devtools-container {
  display: none;
}

</style>