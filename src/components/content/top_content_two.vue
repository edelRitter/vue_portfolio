<template>
  <section id="mainContent">
    <div class="cnt-flex" id="about">
      <div class="cnt-boxes biography">
        <p
        class="cnt-biographytxt fnt-ttl"
        data-aos="fade-right"
        data-aos-duration="800"
        data-aos-delay="200"
        data-aos-once="true">
        /the <span class="fntcolor-red">noblest</span> pleasure is the joy of understanding
        </p>
        <p class="cnt-biographydesc">Hi, my name is Yohei. Based in Tokyo, Japan. Currently working as a frontend engineer at Rakuten. Avid lover of well-crafted minimalism.<br>(Edel Ritter = german for noble knights)</p>
        <div class="cnt-biography-loves">
          <p class="fntcolor-red fntsize-mid">/ loves</p>
          <p class="fntsize-sml">| SOUND : Daft Punk, BT, J.A.M, Jazzanova, Hybrid, Hamauzu Masashi, Quasimode, nujabes, nomak, jinsang, Thomas J. Bergersen, Caravan Palace, etc. Currently in love with lo-fi music and good mash-ups
          <br><br>| FILM : Lawrence of Arabia, The Matrix, Memento, Blade Runner, 2001 : A Space Odyssey, Akira, Inception, Brazil, Metropolis, Truman Show, Up, Spirited Away, The Shape of Water, Mad-max: Fury Road, etc.
          <br><br>| HOBBIES : Drawing Illustrations, coding research and practice.
          </p>
        </div>
        <div class="cnt-biography-loves">
          <p class="fntcolor-red fntsize-mid">/ contact</p>
          <p class="fntsize-sml">| ADDRESS : &#12306; 140-0011 Tokyo Shinagawa District<br>
            | TEL : (080) 6138 0541<br>
            | MAIL : yisshiki@gmail.com
          </p>
        </div>
      </div>
      <div class="cnt-boxes social">
        <p
        class="cnt-social-profile"
        data-aos="fade"
        data-aos-duration="800"
        data-aos-delay="300"
        data-aos-once="true">
        <img src="./images/profile.jpg">
        </p>
        <p class="bdr"></p>
        <div class="cnt-social-wrap">
          <div class="cnt-social-flex">
            <div
            class="cnt-social-icn"
            data-aos="zoom-in"
            data-aos-duration="800"
            data-aos-delay="300"
            data-aos-once="true">
              <p class="twitter"><a href="#"><SvgPathIcon name="twitter_icon" /></a></p>
            </div>
            <div
            class="cnt-social-icn"
            data-aos="zoom-in"
            data-aos-duration="800"
            data-aos-delay="300"
            data-aos-once="true">
              <p class="facebook"><a href="https://github.com/edelRitter"><SvgPathIcon name="github_icon" /></a></p>
            </div>
            <div
            class="cnt-social-icn"
            data-aos="zoom-in"
            data-aos-duration="800"
            data-aos-delay="300"
            data-aos-once="true">
              <p class="mail"><a href="#"><SvgPathIcon name="mail_icon" /></a></p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
#mainContent {
width: 100%;
}
#mainContent .cnt-flex {
display: -webkit-box;
display: -moz-box;
display: -ms-flexbox;
display: -moz-flex;
display: -webkit-flex;
display: flex;
align-items: stretch;
}
#mainContent .cnt-flex .cnt-boxes {
-webkit-flex-wrap: wrap;
flex-wrap: wrap;
box-sizing: border-box;
}
#mainContent .cnt-flex .cnt-boxes.biography {
box-sizing: border-box;
width: 50%;
padding: 80px 2%;
background: #f4f4f4;
}
#mainContent .cnt-flex .cnt-boxes.social {
box-sizing: border-box;
width: 50%;
padding: 0 0 80px 0;
}
#mainContent .cnt-flex .cnt-boxes .cnt-biographytxt {
letter-spacing: 0.2em;
font-family: 'Playfair Display', serif;
}
#mainContent .cnt-flex .cnt-boxes .cnt-biographydesc {
margin: 80px 0 0 0;
font-size: 16px;
line-height: 1.8em;
}
#mainContent .cnt-flex .cnt-boxes .cnt-biography-loves {
display: flex;
margin: 40px 0 0 0;
line-height: 1.8em;
}
#mainContent .cnt-flex .cnt-boxes .cnt-biography-loves p {
width: 80%;
}
#mainContent .cnt-flex .cnt-boxes .cnt-biography-loves p:first-child {
width: 20%;
margin: -2px 0 0 0;
font-family: 'Oswald', 'arial', serif;
}
#mainContent .cnt-social-profile img {
width: 100%;
height: auto;
}
#mainContent .bdr {
clear: both;
position: relative;
width: 10%;
height: 1px;
margin: 80px auto;
background: #333;
}
#mainContent .cnt-flex .cnt-boxes .cnt-social-flex {
display: flex;
justify-content: center;
}
#mainContent .cnt-flex .cnt-social-wrap {
position: relative;
overflow: hidden;
}
#mainContent .cnt-flex .cnt-social-wrap .cnt-social-icn p {
margin: 0 20px;
}
@media only screen and (max-width: 620px) {
  #mainContent .cnt-flex .cnt-boxes {
  font-size: 18px;
  }
  #mainContent .cnt-flex {
  flex-direction: column;
  }
  #mainContent .cnt-flex .cnt-boxes.biography,
  #mainContent .cnt-flex .cnt-boxes.social {
  width: 100%;
  }
  #mainContent .cnt-flex .cnt-boxes.biography {
  padding: 40px 2%;
  }
  #mainContent .bdr {
  margin: 40px auto;
  }
  #mainContent .cnt-flex .cnt-boxes .cnt-biographydesc,
  #mainContent .cnt-flex .cnt-boxes .cnt-biography-loves {
  margin: 40px 0 0 0;
  }
}
</style>

<script>
import SvgPathIcon from './../ui/app_icon.vue'

export default {
  name: 'topSecondcnt',
  data () {
    return {
      iconNames: [
        'twitter_icon',
        'facebook_icon',
        'mail_icon'
      ]
    }
  },
  components: {
    SvgPathIcon
  }
}
</script>
