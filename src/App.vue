<template>
  <div id="app">
    <loader></loader>
    <headerNav></headerNav>
    <topFirstcnt></topFirstcnt>
    <topSecondcnt></topSecondcnt>
    <topThirdcnt></topThirdcnt>
    <topFourthcnt></topFourthcnt>
  </div>
</template>

<script>
import loader from './components/ui/app_loader.vue'
import headerNav from './components/ui/app_header.vue'
import topFirstcnt from './components/content/top_content_one.vue'
import topSecondcnt from './components/content/top_content_two.vue'
import topThirdcnt from './components/content/top_content_three.vue'
import topFourthcnt from './components/content/top_content_four.vue'

export default {
  name: 'App',
  components: {
    'loader': loader,
    'headerNav': headerNav,
    'topFirstcnt': topFirstcnt,
    'topSecondcnt': topSecondcnt,
    'topThirdcnt': topThirdcnt,
    'topFourthcnt': topFourthcnt
  }
}
</script>

<style>

section {
clear: both;
position: relative;
overflow: hidden;
min-height: 100vh;
}
.fntsize-lrg {
font-size: 24px;
}
.fntsize-mid {
font-size: 16px;
}
.fntsize-sml {
font-size: 12px;
}
.fnt-ttl {
font-size: 36px;
}
.fntcolor-red {
color: #c72e53;
}
.seemore {
position: relative;
cursor: pointer;
font-family: 'Oswald', 'arial', serif;
}
.seemore:before {
content: "";
position: absolute;
left: 0;
right: 100%;
bottom: -4px;
background: #c72e53;
height: 1px;
-webkit-transition-property: right;
transition-property: right;
-webkit-transition-duration: 0.3s;
transition-duration: 0.3s;
-webkit-transition-timing-function: ease-out;
transition-timing-function: ease-out;
z-index: -1;
}
.seemore:hover:before {
right: 0;
}
::-webkit-scrollbar {
width: 2px;
}
::-webkit-scrollbar-track {
background: #333;
}
::-webkit-scrollbar-thumb {
background: #c72e53;
}
@media only screen and (max-width: 620px) {
/* universal */
  .fntsize-mid{
    font-size: 14px;
  }
  .fnt-ttl {
    font-size: 28px;
  }
  .sp-nodisplay {
    display: none !important;
  }
}
</style>
