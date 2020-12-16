<template>
<section id="portfolio">
  <div id="works"></div>
	<p class="select-work"><span class="fnt-ttl">/</span><span class="fnt-ttl">selected<br />works</span></p>
  <div class="works-wrap">
    <div
      class="fnt-ttl works-intro-cnt-ttl"
      data-aos="fade-zoom-in"
      data-aos-duration="1200"
      data-aos-delay="300">
        <span @click="openModal">/01</span>
    </div>
    <div class="works-intro">
      <div class="works-flex">
        <div class="works-intro-bg">
          <p
          data-aos="fade-left"
          data-aos-duration="1200"
          data-aos-delay="300"
          class="works-one">
          </p>
        </div>
        <div
        class="works-desc-wrap"
        data-aos="fade-right"
        data-aos-duration="1200"
        data-aos-delay="300">
          <div class="works-desc">
            <p class="works-desc-ttl">/ 2018 <br class="sp-nodisplay" />Japan Photography <br class="sp-nodisplay" />Showcase</p>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam ultricies justo eros, ac efficitur lacus eleifend eu. Cras rhoncus lorem ipsum, non sodales diam blandit vitae. Nullam auctor pharetra elit, quis tincidunt tellus venenatis at. Praesent molestie accumsan blandit. </p>
          </div>
        </div>
      </div>
    </div>
    <ModalComponent ref="modal">
      <template v-slot:modalTitleOne>My Image’s Title</template>
      <template v-slot:modalImgOne><img src="./images/shimane_work1.png"></template>
      <template v-slot:modalTitleTwo>My Image’s Title</template>
      <template v-slot:modalImgTwo><img src="./images/shimane_work3.png"></template>
    </ModalComponent>
  </div>
  <p class="works-bdr"></p>
  <div class="works-wrap">
    <div class="works-intro">
      <div
      class="fnt-ttl works-intro-cnt-ttl"
      data-aos="fade-zoom-in"
      data-aos-duration="1200"
      data-aos-delay="300">
        <span @click="openModal">/02</span>
      </div>
      <div class="works-flex">
        <div class="works-intro-bg">
          <p
          class="works-two"
          data-aos="fade-left"
          data-aos-duration="1200"
          data-aos-delay="300">
          </p>
        </div>
        <div
        class="works-desc-wrap"
        data-aos="fade-right"
        data-aos-duration="1200"
        data-aos-delay="300">
          <div class="works-desc">
            <p class="works-desc-ttl">/ 2019 <br class="sp-nodisplay" />Design Works <br class="sp-nodisplay" />Showcase</p>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam ultricies justo eros, ac efficitur lacus eleifend eu. Cras rhoncus lorem ipsum, non sodales diam blandit vitae. Nullam auctor pharetra elit, quis tincidunt tellus venenatis at. Praesent molestie accumsan blandit. </p>
          </div>
        </div>
      </div>
    </div>
    <ModalComponent ref="modal">
      <template v-slot:modalTitleOne>test</template>
      <template v-slot:modalImgOne><img src="./images/shimane_work1.png"></template>
      <template v-slot:modalTitleTwo>test</template>
      <template v-slot:modalImgTwo><img src="./images/shimane_work3.png"></template>
    </ModalComponent>
  </div>
  <p class="works-bdr"></p>
  <div class="works-wrap">
    <div class="works-intro">
      <div
      class="fnt-ttl works-intro-cnt-ttl"
      data-aos="fade-zoom-in"
      data-aos-duration="1200"
      data-aos-delay="300">
        <span @click="openModal">/03</span>
      </div>
      <div class="works-flex">
        <div class="works-intro-bg">
          <p
          class="works-two"
          data-aos="fade-left"
          data-aos-duration="1200"
          data-aos-delay="300">
          </p>
        </div>
        <div
        class="works-desc-wrap"
        data-aos="fade-right"
        data-aos-duration="1200"
        data-aos-delay="300">
          <div class="works-desc">
            <p class="works-desc-ttl">/ 2019 <br class="sp-nodisplay" />Illustration Works <br class="sp-nodisplay" />Showcase</p>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam ultricies justo eros, ac efficitur lacus eleifend eu. Cras rhoncus lorem ipsum, non sodales diam blandit vitae. Nullam auctor pharetra elit, quis tincidunt tellus venenatis at. Praesent molestie accumsan blandit. </p>
          </div>
        </div>
      </div>
    </div>
    <ModalComponent ref="modal">
      <template v-slot:modalTitleOne>test</template>
      <template v-slot:modalImgOne><img src="./images/shimane_work1.png"></template>
      <template v-slot:modalTitleTwo>test</template>
      <template v-slot:modalImgTwo><img src="./images/shimane_work3.png"></template>
    </ModalComponent>
  </div>
</section>
</template>

<style scoped>
#portfolio {
color: #fff;
background: #333;
z-index: 3;
}
#portfolio .select-work {
clear: both;
box-sizing: border-box;
width: 100%;
text-align: center;
margin: 120px auto;
padding: 0 2%;
}
#portfolio .select-work span {
letter-spacing: 0.4em;
font-family: 'Playfair Display', serif;
}
#portfolio .works-wrap {
position: relative;
}
#portfolio .works-intro {
position: relative;
box-sizing: border-box;
width: 100%;
}
#portfolio .works-intro:after {
content: '';
display: block;
height: 1px;
position: absolute;
width: 10%;
bottom: -40px;
margin: 0px auto;
left: 0;
right: 0;
background: #c72e53;
}
#portfolio .works-intro:last-child:after {
content: '';
display: none;
}
#portfolio .works-intro-cnt-ttl {
position: absolute;
top: 25%;
text-indent: 6%;
width: 100%;
text-align: center;
font-size: 20vw;
color: transparent;
-webkit-text-stroke: 0.2vw #c72e53;
text-stroke: 0.2vw #c72e53;
letter-spacing: 0.6em;
font-family: 'Oswald', 'arial', serif;
z-index: 1;
}
#portfolio .works-intro-cnt-ttl span {
cursor: pointer;
}
#portfolio .works-flex {
clear: both;
display: flex;
}
#portfolio .works-flex > div  {
clear: both;
position: relative;
box-sizing: border-box;
width: 50%;
}
#portfolio .works-flex .works-desc-wrap {
position: relative;
box-sizing: border-box;
padding: 0 2%;
color: #fff;
}
#portfolio .works-flex .works-desc-wrap .works-desc-ttl {
margin: 0 0 40px 0;
font-size: 4vw;
line-height: 1.2em;
font-family: 'Playfair Display', serif;
}
#portfolio .works-flex .works-intro-bg p.works-one {
background: url("./images/work-top.png") no-repeat;
background-size: cover;
background-position: bottom center;
width: 100%;
height: 100vh;
}
#portfolio .works-flex .works-intro-bg p.works-two {
background: url("./images/demo_design.png") no-repeat;
background-size: cover;
background-position: bottom center;
width: 100%;
height: 100vh;
}
#portfolio .works-bdr {
height: 1px;
width: 25%;
margin: 40px auto;
background: #c72e53;
}
@media only screen and (max-width: 620px) {
  #portfolio .works-intro {
  width: 100%;
  }
  #portfolio .works-flex {
  flex-direction: column;
  }
  #portfolio .works-flex > div,
  #portfolio .works-flex .works-desc-wrap {
  width: 100%;
  margin: 0;
  }
  #portfolio .works-flex .works-desc-wrap {
  padding: 12px;
  line-height: 1.6em;
  color: #333;
  background: #f4f4f4;
  }
  #portfolio .works-flex .works-desc-wrap .works-desc-ttl {
  margin: 20px auto;
  }
  #portfolio .works-flex .works-intro-bg p {
  height: 50vh !important;
  }
  #portfolio .seemore {
  position: relative;
  bottom: 0;
  margin: 20px 0;
  }
}
</style>

<script>
import ModalComponent from './../ui/app_modal.vue'

export default {
  name: 'topThirdcnt',
  components: {
    ModalComponent
  },
  methods: {
    toggler () {
      this.isActive = !this.isActive
    },
    openModal () {
      this.$refs.modal.show()
    }
  }
}
</script>
