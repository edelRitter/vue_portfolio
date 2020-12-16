<template>
  <transition name="modal-fade">
  <div
  class="works-modal"
  v-if="showModal"
  v-bind:class="{ 'modal-on' : showModal }">
    <p class="modal-closebtn" @click="hide">
      <span></span>
      <span></span>
    </p>
    <div class="modal-works">
      <div class="modal-img">
        <slot name="modalImgOne"></slot>
        <slot name="modalTitleOne">FreeWork</slot>
      </div>
      <div class="modal-img">
        <slot name="modalImgTwo"></slot>
        <slot name="modalTitleTwo">FreeWork</slot>
      </div>
    </div>
  <div class="modalbg" v-bind:class="{ 'modal-on' : showModal }"></div>
  </div>
  </transition>
</template>

<style>
.modal-fade-enter,
.modal-fade-leave-active {
opacity: 0;
}
.modal-fade-enter-active,
.modal-fade-leave-active {
transition: opacity .5s ease
}
.works-modal {
position: fixed;
top: 0;
left: 0;
height: 100%;
width: 100%;
display: block;
z-index: 9;
}
.modal-closebtn {
position: fixed;
top: 50%;
right: 0;
width: 40px;
height: 40px;
overflow-y: auto;
cursor: pointer;
z-index: 11;
}
.modal-closebtn span {
display: block;
position: absolute;
top: 20px;
left: 6px;
width: 30px;
height: 2px;
background: #fff;
-webkit-transform: rotate(45deg);
-moz-transform: rotate(45deg);
-o-transform: rotate(45deg);
transform: rotate(45deg);
}
.modal-closebtn span:last-child {
-webkit-transform: rotate(-45deg);
-moz-transform: rotate(-45deg);
-o-transform: rotate(-45deg);
transform: rotate(-45deg);
}
.modal-works {
position: relative;
overflow: auto;
width: 75%;
height: 100%;
color: #333;
background: #fff;
z-index: 10;
}
.modal-works .modal-img {
width: 100%;
margin: 40px auto;
}
.modal-works .modal-img img {
width: 100%;
max-width: 800px;
height: auto;
}
.works-modal .modalbg{
position: absolute;
top: 0;
left: 0;
width: 100%;
height: 100vh;
opacity: 0.5;
background: #000;
z-index: 0;
}
@media only screen and (max-width: 620px) {
  .modal-works {
    width: 92%;
  }
}
</style>

<script>
export default {
  name: 'ModalComponent',
  data () {
    return {
      showModal: false
    }
  },
  methods: {
    show () {
      this.showModal = !this.showModal
    },
    hide () {
      this.showModal = false
    }
  }
}
</script>
