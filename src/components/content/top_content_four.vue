<template>
<section id="contact">
  <div class="contact-txt">
  <p class="fnt-ttl">/ contact</p>
  </div>
  <div class="contact-sns">
    <div class="sns-txt">
      <p class="fnt-ttl"><img src="./images/logo.png" width="100%"></p>
      <div class="contact-wrap">
      <div class="cnt-social-flex">
        <div
        class="cnt-social-icn"
        data-aos="zoom-in"
        data-aos-duration="800"
        data-aos-delay="300">
          <p class="twitter"><a href="#"><SvgPathIcon name="twitter_icon" /></a></p>
        </div>
        <div
        class="cnt-social-icn"
        data-aos="zoom-in"
        data-aos-duration="800"
        data-aos-delay="300">
          <p class="facebook"><a href="https://github.com/edelRitter"><SvgPathIcon name="github_icon" /></a></p>
        </div>
        <div
        class="cnt-social-icn"
        data-aos="zoom-in"
        data-aos-duration="800"
        data-aos-delay="300">
          <p class="mail"><a href="#"><SvgPathIcon name="mail_icon" /></a></p>
        </div>
      </div>
    </div>
    </div>
  </div>
  <div class="copyright"><p>© Yohei Isshiki</p></div>
</section>
</template>

<style scoped>
#contact {
clear: both;
}
#contact .contact-txt {
clear: both;
margin: 120px auto;
text-align: center;
font-family: 'Playfair Display', serif;
}
#contact .contact-sns {
clear: both;
display: flex;
width: 50%;
margin: 20px auto;
align-items: stretch;
justify-content: center;
font-family: 'Oswald', 'arial', serif;
}
#contact .contact-wrap {
margin: 0 auto 40px;
}
#contact .contact-wrap .cnt-social-flex {
display: flex;
align-items: center;
justify-content: center;
margin: 40px auto;
}
#contact .contact-wrap .cnt-social-flex .cnt-social-icn p {
margin: 0 20px;
}
#contact .copyright {
clear: both;
position: absolute;
bottom: 0;
left: 2%;
}
</style>

<script>
import SvgPathIcon from './../ui/app_icon.vue'

export default {
  name: 'topFourthcnt',
  components: {
    SvgPathIcon
  }
}
</script>
