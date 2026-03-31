<template>
  <svg width="570" height="130" viewBox="0 0 570 130" class="sparkline-chart">
    <!-- init -->
    <rect x="10" y="72" width="44" height="7" fill="#999"/>
    <rect x="10" y="81" width="44" height="6" fill="#999"/>
    <!-- search -->
    <rect x="75" y="64" width="44" height="7" fill="#999"/>
    <rect x="75" y="73" width="44" height="6" fill="#999"/>
    <rect x="75" y="81" width="44" height="6" fill="#999"/>
    <!-- add -->
    <rect x="140" y="54" width="44" height="7" fill="#999"/>
    <rect x="140" y="63" width="44" height="7" fill="#999"/>
    <rect x="140" y="72" width="44" height="7" fill="#999"/>
    <rect x="140" y="81" width="44" height="6" fill="#999"/>
    <!-- lock -->
    <rect x="205" y="37" width="44" height="7" fill="#888"/>
    <rect x="205" y="46" width="44" height="7" fill="#888"/>
    <rect x="205" y="55" width="44" height="6" fill="#888"/>
    <rect x="205" y="63" width="44" height="7" fill="#888"/>
    <rect x="205" y="72" width="44" height="7" fill="#888"/>
    <rect x="205" y="81" width="44" height="6" fill="#888"/>
    <!-- install -->
    <rect x="270" y="30" width="44" height="7" fill="#888"/>
    <rect x="270" y="39" width="44" height="6" fill="#888"/>
    <rect x="270" y="47" width="44" height="6" fill="#888"/>
    <rect x="270" y="55" width="44" height="6" fill="#888"/>
    <rect x="270" y="63" width="44" height="7" fill="#888"/>
    <rect x="270" y="72" width="44" height="7" fill="#888"/>
    <rect x="270" y="81" width="44" height="6" fill="#888"/>
    <!-- shell -->
    <rect x="335" y="47" width="44" height="6" fill="#999"/>
    <rect x="335" y="55" width="44" height="6" fill="#999"/>
    <rect x="335" y="63" width="44" height="7" fill="#999"/>
    <rect x="335" y="72" width="44" height="7" fill="#999"/>
    <rect x="335" y="81" width="44" height="6" fill="#999"/>
    <!-- run -->
    <rect x="400" y="52" width="44" height="7" fill="#999"/>
    <rect x="400" y="61" width="44" height="7" fill="#999"/>
    <rect x="400" y="72" width="44" height="7" fill="#999"/>
    <rect x="400" y="81" width="44" height="6" fill="#999"/>
    <!-- build -->
    <rect x="465" y="22" width="44" height="7" fill="#a00000"/>
    <rect x="465" y="31" width="44" height="6" fill="#a00000"/>
    <rect x="465" y="39" width="44" height="6" fill="#a00000"/>
    <rect x="465" y="47" width="44" height="6" fill="#a00000"/>
    <rect x="465" y="55" width="44" height="6" fill="#a00000"/>
    <rect x="465" y="63" width="44" height="7" fill="#a00000"/>
    <rect x="465" y="72" width="44" height="7" fill="#a00000"/>
    <rect x="465" y="81" width="44" height="6" fill="#a00000"/>
    <!-- Labels -->
    <text x="32"  y="102" text-anchor="middle" style="font-size:12px!important;font-family:'IBM Plex Mono',monospace!important;line-height:normal!important;" fill="#888">init</text>
    <text x="97"  y="102" text-anchor="middle" style="font-size:12px!important;font-family:'IBM Plex Mono',monospace!important;line-height:normal!important;" fill="#888">search</text>
    <text x="162" y="102" text-anchor="middle" style="font-size:12px!important;font-family:'IBM Plex Mono',monospace!important;line-height:normal!important;" fill="#888">add</text>
    <text x="227" y="102" text-anchor="middle" style="font-size:12px!important;font-family:'IBM Plex Mono',monospace!important;line-height:normal!important;" fill="#888">lock</text>
    <text x="292" y="102" text-anchor="middle" style="font-size:12px!important;font-family:'IBM Plex Mono',monospace!important;line-height:normal!important;" fill="#888">install</text>
    <text x="357" y="102" text-anchor="middle" style="font-size:12px!important;font-family:'IBM Plex Mono',monospace!important;line-height:normal!important;" fill="#888">shell</text>
    <text x="422" y="102" text-anchor="middle" style="font-size:12px!important;font-family:'IBM Plex Mono',monospace!important;line-height:normal!important;" fill="#888">run</text>
    <text x="487" y="102" text-anchor="middle" style="font-size:12px!important;font-family:'IBM Plex Mono',monospace!important;line-height:normal!important;" fill="#a00000">build</text>
  </svg>
</template>

<style scoped>
.sparkline-chart {
  margin-top: 0.5rem;
  display: block;
}
.sparkline-chart text {
  font-size: 12px !important;
  font-family: 'IBM Plex Mono', monospace !important;
  line-height: normal !important;
}
</style>
