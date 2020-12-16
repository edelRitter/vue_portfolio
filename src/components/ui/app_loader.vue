<template>
  <div id="rjs-loader">
    <div class="loader-wrap">
      <p class="loader-ttl">
        <span>e</span>
        <span>d</span>
        <span>e</span>
        <span>l</span>
        <span>R</span>
      </p>
    </div>
    <div id="rjs-loader-effect">
      <!-- エフェクトの影響を受けたいコンテンツはこの中へ -->
    </div>
  </div>
</template>

<style scoped>
#rjs-loader {
	display: flex;
	flex-wrap: wrap;
	position: fixed;
	justify-content: center;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
	opacity: 0;
	visibility: hidden;
	z-index: 9999;
}
#rjs-loader.loader-on {
	opacity: 1;
	visibility: visible;
}
#rjs-loader.animation-finished {
	visibility: hidden;
	opacity: 0;
}
#rjs-loader-effect {
	position: absolute;
	margin: auto;
	width: 100%;
	height: 100%;
	top: 0;
	left: 0;
	bottom: 0;
	right: 0;
	background: #333;
	z-index: 1;
}
#rjs-loader .loader-wrap {
  position: absolute;
	margin: auto;
	padding: 0;
	width: 100%;
	height: 100%;
	top: 0;
	left: 0;
	bottom: 0;
  right: 0;
  -webkit-animation: fade-out-bck 0.4s cubic-bezier(0.250, 0.460, 0.450, 1) both 1.8s;
	animation: fade-out-bck 0.4s cubic-bezier(0.250, 0.460, 0.450, 1) both 1.8s;
	z-index: 2;
}
.loader-ttl {
  display: flex;
  justify-content: center;
  font-size: 5vw;
  line-height: 100vh;
	color: #fff;
	text-align: center;
	font-family: 'Playfair Display', serif;
  -webkit-animation: tracking-in-expand 1.4s cubic-bezier(0.215, 0.610, 0.355, 1.000) both 0.4s;
  animation: tracking-in-expand 1.4s cubic-bezier(0.215, 0.610, 0.355, 1.000) both 0.4s;
}
.loader-ttl span {
  margin: 0 5%;
}
.rld-fade-out {
-webkit-animation: fade-out-bck 0.4s cubic-bezier(0.250, 0.460, 0.450, 1) both;
animation: fade-out-bck 0.4s cubic-bezier(0.250, 0.460, 0.450, 1) both;
}
.rld-left-out {
-webkit-animation: scale-out-hor-left 0.4s cubic-bezier(0.550, 0.085, 0.680, 0.530) both;
animation: scale-out-hor-left 0.4s cubic-bezier(0.550, 0.085, 0.680, 0.530) both;
}
.rld-right-out {
-webkit-animation: scale-out-hor-right 0.4s cubic-bezier(0.550, 0.085, 0.680, 0.530) both;
animation: scale-out-hor-right 0.4s cubic-bezier(0.550, 0.085, 0.680, 0.530) both;
}
.rld-top-out {
-webkit-animation: slide-out-bottom 0.4s cubic-bezier(0.550, 0.085, 0.680, 0.530) both;
animation: slide-out-bottom 0.4s cubic-bezier(0.550, 0.085, 0.680, 0.530) both;
}
.rld-bottom-out {
-webkit-animation: slide-out-top 0.4s cubic-bezier(0.550, 0.085, 0.680, 0.530) both;
animation: slide-out-top 0.4s cubic-bezier(0.550, 0.085, 0.680, 0.530) both;
}

@-webkit-keyframes fade-out-bck{0%{transform:translateZ(0);opacity:1}100%{transform:translateZ(-80px);opacity:0}}
@keyframes fade-out-bck{0%{transform:translateZ(0);opacity:1}100%{transform:translateZ(-80px);opacity:0}}
@-webkit-keyframes scale-out-hor-left{0%{transform:scaleX(1);transform-origin:0 0;opacity:1}100%{transform:scaleX(0);transform-origin:0 0;opacity:1}}
@keyframes scale-out-hor-left{0%{transform:scaleX(1);transform-origin:0 0;opacity:1}100%{transform:scaleX(0);transform-origin:0 0;opacity:1}}
@-webkit-keyframes scale-out-hor-right{0%{transform:scaleX(1);transform-origin:100% 100%;opacity:1}100%{transform:scaleX(0);transform-origin:100% 100%;opacity:1}}
@keyframes scale-out-hor-right{0%{transform:scaleX(1);transform-origin:100% 100%;opacity:1}100%{transform:scaleX(0);transform-origin:100% 100%;opacity:1}}
@-webkit-keyframes slide-out-bottom{0%{transform:translateY(0);opacity:1}100%{transform:translateY(1000px);opacity:0}}
@keyframes slide-out-bottom{0%{transform:translateY(0);opacity:1}100%{transform:translateY(1000px);opacity:0}}
@-webkit-keyframes slide-out-top{0%{transform:translateY(0);opacity:1}100%{transform:translateY(-1000px);opacity:0}}
@keyframes slide-out-top{0%{transform:translateY(0);opacity:1}100%{transform:translateY(-1000px);opacity:0}}
@-webkit-keyframes tracking-in-expand{0%{letter-spacing:-.5em;opacity:0}40%{opacity:.6}100%{opacity:1}}
@keyframes tracking-in-expand{0%{letter-spacing:-.5em;opacity:0}40%{opacity:.6}100%{opacity:1}}
</style>

<script>
export default {
  name: 'loader',
  mounted () {
    const rLoader = document.getElementById('rjs-loader')
    const rLoaderType = document.getElementById('rjs-loader-effect')
    let ldr = {
      animationwait: 'false',
      animationtrigger: 'always',
      animationspeed: 2600,
      animationtype: 'rld-left-out'
    }
    /* loading animation - type */
    setTimeout(function () {
      rLoaderType.classList.add(ldr.animationtype)
    }, ldr.animationspeed - 600)

    /* loading animation - trigger */
    if (ldr.animationtrigger === 'always' || ldr.animationtrigger === 'once') {
      rLoader.classList.add('loader-on')
      setTimeout(function () {
        rLoader.classList.add('animation-finished')
        window.sessionStorage.setItem('ldr-triggered', true)
      }, ldr.animationspeed)
    }
    if ((ldr.animationtrigger === 'once' && window.sessionStorage.getItem('ldr-triggered')) || (ldr.animationtrigger === 'off')) {
      rLoader.parentNode.removeChild(rLoader)
    } else {
    }
  }
}
</script>
