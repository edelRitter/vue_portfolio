<template>
  <section id="mainTtl">
    <div class="ttl-hero">
      <div
      class="ttl-caption fnt-ttl"
      data-aos="fade-right"
      data-aos-duration="800"
      data-aos-delay="2400"
      data-aos-once="true">
        <span>/ welcome </span><span>/ to </span><span>/ the /</span><br /><span>/ ROUND </span><span>/ TABLE /</span>
      </div>
      <div class="ttl-logo"></div>
    </div>
  </section>
</template>

<style scoped>
#mainTtl .ttl-hero {
background: url("./images/daftpunk.png") no-repeat;
background-size: cover;
background-position: center center;
width: 100%;
height: 100vh;
}
#mainTtl .ttl-caption {
position: absolute;
box-sizing: border-box;
top: 40%;
width: 75%;
padding: 2%;
color: #fff;
font-size: 52px;
font-family: 'Playfair Display', serif;
z-index: 2;
}
#mainTtl .ttl-logo {
position: absolute;
box-sizing: border-box;
top: 25%;
right: 10%;
width: 25%;
height: 50vh;
background: url('./images/logo_design.png') no-repeat;
background-size: contain;
background-position: center center;
z-index: 1;
}
@media only screen and (max-width: 620px) {
  #mainTtl .ttl-logo {
  width: 100%;
  right: 0;
  height: 25vh;
  top: 25%;
  }
  #mainTtl .ttl-caption {
  font-size: 28px;
  width: 96%;
  margin: 0 0 0 2%;
  top: 50%;
  }
}
</style>

<script>
export default {
  name: 'topFirstcnt'
}
</script>
