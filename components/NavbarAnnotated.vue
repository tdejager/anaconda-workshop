<template>
  <div class="navbar-annotated">
    <img src="/book-navbar.png" class="navbar-img" alt="Book navbar" />
    <svg class="annotations" viewBox="0 0 900 160" preserveAspectRatio="xMidYMid meet">
      <defs>
        <marker id="arrowhead" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
          <polygon points="0 0, 8 3, 0 6" fill="#a00000" />
        </marker>
      </defs>
      <!-- Focus mode arrow -->
      <line x1="420" y1="120" x2="462" y2="52" stroke="#a00000" stroke-width="1.5" marker-end="url(#arrowhead)" />
      <text x="420" y="138" text-anchor="middle" style="font-size:13px!important;font-family:'IBM Plex Mono',monospace!important;line-height:normal!important;" fill="#a00000">Focus mode</text>
      <!-- Source viewer arrow -->
      <line x1="545" y1="120" x2="502" y2="52" stroke="#a00000" stroke-width="1.5" marker-end="url(#arrowhead)" />
      <text x="545" y="138" text-anchor="middle" style="font-size:13px!important;font-family:'IBM Plex Mono',monospace!important;line-height:normal!important;" fill="#a00000">Source viewer</text>
      <!-- Theme toggle arrow -->
      <line x1="665" y1="120" x2="540" y2="52" stroke="#a00000" stroke-width="1.5" marker-end="url(#arrowhead)" />
      <text x="665" y="138" text-anchor="middle" style="font-size:13px!important;font-family:'IBM Plex Mono',monospace!important;line-height:normal!important;" fill="#a00000">Theme toggle</text>
    </svg>
  </div>
</template>

<style scoped>
.navbar-annotated {
  position: relative;
  width: 100%;
  max-width: 700px;
}
.navbar-img {
  width: 100%;
  border: 1px solid #e0d8c8;
  border-radius: 4px;
  display: block;
}
.annotations {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  pointer-events: none;
}
.annotations text {
  font-size: 13px !important;
  font-family: 'IBM Plex Mono', monospace !important;
  line-height: normal !important;
}
</style>
