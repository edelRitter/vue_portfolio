<template>
  <nav
  id="allnav"
  class="nav-default"
  :class="{ 'nav-white': !showNavbar }">
    <div class="nav_logo"><a href="http://edelritter.github.io/portfolio"></a></div>
    <div class="nav_hamburger">
      <div class="nav_btn" v-on:click="toggler" v-bind:class="{ 'nav_active' : isActive }">
        <span></span><span></span><span></span><span></span>
      </div>
    </div>
    <div class="nav_wrap" v-bind:class="{ 'nav_active' : isActive }">
      <div class="nav_content">
        <p class="nav_list"><a href="#about" v-on:click="toggler" v-bind:class="{ 'nav_active' : isActive }"><span class="mini_txt">01 </span>/ about</a></p>
        <p class="nav_list"><a href="#works" v-on:click="toggler" v-bind:class="{ 'nav_active' : isActive }"><span class="mini_txt">02 </span>/ works</a></p>
        <p class="nav_list"><a href="#contact" v-on:click="toggler" v-bind:class="{ 'nav_active' : isActive }"><span class="mini_txt">03 </span>/ contact</a></p>
      </div>
      <div class="cnt-social-icn">
        <p><a href="#"><SvgPathIcon name="twitter_icon" /></a></p>
        <p><a href="https://github.com/edelRitter"><SvgPathIcon name="github_icon" /></a></p>
      </div>
    </div>
    <div class="nav_bg" v-bind:class="{ 'nav_active' : isActive }"></div>
  </nav>
</template>

<style scoped>
#allnav {
position: fixed;
top: 0;
right: 0;
width: 100%;
-webkit-animation: slide_in_top 1.6s cubic-bezier(0.770, 0.000, 0.175, 1.000) both 2s;
animation: slide_in_top 1.6s cubic-bezier(0.770, 0.000, 0.175, 1.000) both 2s;
z-index: 999;
}
#allnav .nav_logo {
background: url('logo.png') no-repeat;
background-size: 114px 18px;
width: 114px;
height: 18px;
margin: 11px 0 11px 2%;
-webkit-transition: .25s ease-in-out;
-moz-transition: .25s ease-in-out;
-o-transition: .25s ease-in-out;
transition: .25s ease-in-out;
}
#allnav .nav_logo a {
display: block;
width: 100%;
height: 100%;
cursor: pointer;
}
#allnav #nav_menu {
background: #ccc;
padding: 4px;
}
.nav_hamburger {
position: absolute;
top: 0;
right: 0;
width: 44px;
height: 40px;
padding: 4px;
}
.nav_hamburger {
width: 44px;
height: 40px;
padding: 4px;
-webkit-transform: rotate(0deg);
-moz-transform: rotate(0deg);
-o-transform: rotate(0deg);
transform: rotate(0deg);
-webkit-transition: .5s ease-in-out;
-moz-transition: .5s ease-in-out;
-o-transition: .5s ease-in-out;
transition: .5s ease-in-out;
cursor: pointer;
z-index: 2;
}
.nav_hamburger>div {
display: block;
width: 100%;
height: 100%;
}
.nav_hamburger span {
display: block;
position: absolute;
height: 1px;
width: 28px;
background: #333;
opacity: 1;
left: 8px;
-webkit-transform: rotate(0deg);
-moz-transform: rotate(0deg);
-o-transform: rotate(0deg);
transform: rotate(0deg);
-webkit-transition: .25s ease-in-out;
-moz-transition: .25s ease-in-out;
-o-transition: .25s ease-in-out;
transition: .25s ease-in-out;
}
.nav_hamburger span:nth-child(1) {
top: 12px;
}
.nav_hamburger span:nth-child(2), .nav_hamburger span:nth-child(3) {
top: 19px;
}
.nav_hamburger span:nth-child(4) {
top: 26px;
}
.nav_hamburger .nav_active span:nth-child(1) {
top: 18px;
width: 0%;
left: 50%;
}
.nav_hamburger .nav_active span:nth-child(2) {
-webkit-transform: rotate(45deg);
-moz-transform: rotate(45deg);
-o-transform: rotate(45deg);
transform: rotate(45deg);
}
.nav_hamburger .nav_active span:nth-child(3) {
-webkit-transform: rotate(-45deg);
-moz-transform: rotate(-45deg);
-o-transform: rotate(-45deg);
transform: rotate(-45deg);
}
.nav_hamburger .nav_active span:nth-child(4) {
top: 18px;
width: 0%;
left: 50%;
}
.nav_wrap {
position: fixed;
top: 0;
right: 0;
width: 50%;
height: 100vh;
font-size: 14px;
background: #fff;
-webkit-transform: translatex(100%);
-moz-transform: translatex(100%);
-ms-transform: translatex(100%);
-o-transform: translatex(100%);
transform: translatex(100%);
-webkit-transition: transform 0.6s;
-moz-transition: transform 0.6s;
-ms-transition: transform 0.6s;
-o-transition: transform 0.6s;
transition: transform 0.6s;
z-index: 1;
}
.nav_wrap.nav_active {
-webkit-transform: translatex(0);
-moz-transform: translatex(0);
-ms-transform: translatex(0);
-o-transform: translatex(0);
transform: translatex(0);
}
.nav_bg {
position: absolute;
top: 0;
left: 0;
width: 100%;
height: 100vh;
background: #000;
visibility: hidden;
transition: visibility 1s ease, opacity 0.3s linear;
opacity: 0;
}
.nav_bg.nav_active {
visibility: visible;
opacity: 0.5;
}
.nav_wrap .nav_content {
position: relative;
overflow: hidden;
text-align: left;
padding: 40px 0 20px 0;
}
.nav_wrap .nav_content .nav_list {
position: relative;
width: 85%;
padding: 20px 0;
margin: 20px auto;
font-size: 4vw;
font-family: 'Playfair Display', serif;
border-bottom: 1px solid #333;
}
.nav_wrap .nav_content .nav_list a {
display: block;
width: 100%;
height: auto;
}
.nav_wrap .nav_content .nav_list a:hover {
color: #c72e53;
}
.nav_wrap .nav_content .nav_list a:after {
content: '';
position: absolute;
display: block;
left: 0;
bottom: -2px;
width: 0;
height: 2px;
background: #c72e53;
-webkit-transition: all 1s;
transition: all 1s;
}
.nav_wrap .nav_content .nav_list a:hover:after {
width: 100%;
}
.nav_wrap .nav_content .nav_list span {
font-size: 2vw;
}
.nav_wrap .cnt-social-icn p{
margin: 2% 7%;
}
#allnav.nav-white .nav_logo {
background: url('logo_white.png') no-repeat;
background-size: 114px 18px;
}
#allnav.nav-white .nav_hamburger span {
background: #fff;
}
#allnav.nav-white .nav_hamburger .nav_active span {
background: #333;
}
@media only screen and (max-width: 620px) {
  .nav_wrap .nav_content .nav_list span {
  font-size: 4vw;
  }
  .nav_wrap .cnt-social-icn p {
  margin: 25% auto;
  }
}
@-webkit-keyframes slide_in_top {
  0% {
  -webkit-transform: translateY(-1000px);
  transform: translateY(-1000px);
  opacity: 0;
  }
  100% {
  -webkit-transform: translateY(0);
  transform: translateY(0);
  opacity: 1;
  }
}
@keyframes slide_in_top {
  0% {
  -webkit-transform: translateY(-1000px);
  transform: translateY(-1000px);
  opacity: 0;
  }
  100% {
  -webkit-transform: translateY(0);
  transform: translateY(0);
  opacity: 1;
  }
}
</style>

<script>
import SvgPathIcon from './../ui/app_icon.vue'

export default {
  name: 'headerNav',
  data: function () {
    return {
      isActive: false,
      iconNames: [
        'twitter_icon',
        'facebook_icon',
        'mail_icon'
      ],
      showNavbar: false,
      lastScrollPosition: 0
    }
  },
  components: {
    SvgPathIcon
  },
  methods: {
    toggler: function () {
      this.isActive = !this.isActive
    },
    handleScroll: function () {
      let currentScrollPosition = window.pageYOffset
      let sections = document.getElementById('app').getElementsByTagName('section')
      if ((currentScrollPosition < sections[0].clientHeight || currentScrollPosition > sections[2].offsetTop) && (currentScrollPosition < sections[3].offsetTop)) {
        this.showNavbar = false
      } else {
        this.showNavbar = true
      }
    }
  },
  mounted () {
    this.lastScrollPosition = window.pageYOffset
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeDestroy () {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>
