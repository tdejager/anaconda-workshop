<template>
  <div class="navbar-annotated">
    <img src="/book-navbar.png" class="navbar-img" alt="Book navbar" />
    <svg class="annotations" viewBox="0 0 1280 100" preserveAspectRatio="xMidYMid meet">
      <defs>
        <marker id="arr" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
          <polygon points="0 0, 8 3, 0 6" fill="#a00000" />
        </marker>
      </defs>
      <!-- Focus mode: icon center at x=628, y=24 -->
      <line x1="460" y1="85" x2="625" y2="50" stroke="#a00000" stroke-width="2" marker-end="url(#arr)" />
      <text x="455" y="92" text-anchor="end" style="font-size:17px!important;font-family:'IBM Plex Mono',monospace!important;line-height:normal!important;" fill="#a00000">Focus mode</text>
      <!-- Source viewer: icon center at x=677, y=24 -->
      <line x1="850" y1="85" x2="680" y2="50" stroke="#a00000" stroke-width="2" marker-end="url(#arr)" />
      <text x="855" y="92" text-anchor="start" style="font-size:17px!important;font-family:'IBM Plex Mono',monospace!important;line-height:normal!important;" fill="#a00000">Source viewer</text>
    </svg>
  </div>
</template>

<style scoped>
.navbar-annotated {
  position: relative;
  width: 100%;
  max-width: 800px;
}
.navbar-img {
  width: 100%;
  border: 1px solid #e0d8c8;
  border-radius: 4px;
  display: block;
}
.annotations {
  width: 100%;
  display: block;
  margin-top: -2px;
}
.annotations text {
  font-size: 17px !important;
  font-family: 'IBM Plex Mono', monospace !important;
  line-height: normal !important;
}
</style>
