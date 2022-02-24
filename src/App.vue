<template>
  <div id="app" :class="{ 'scroll-off': scrollOff }">
    <Header />
    <Slides />
    <Collections />
    <Banner />
    <!-- <Modal /> -->
    <Footer />
  </div>
</template>

<script>
import Header from "@/components/layout/Header.vue";
import Slides from "@/components/slider/Slides.vue";
import Collections from "@/components/collections/Collections.vue";
import Banner from "@/components/banner/Banner";
import Modal from "@/components/modal/Modal";
import Footer from "@/components/layout/Footer";
export default {
  name: "app",
  components: { Header, Slides, Collections, Banner, Modal, Footer },
  data() {
    return {
      scrollOff: false,
    };
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");
@font-face {
  font-family: "Didot";
  src: local("Didot"),
    url("/fonts/Didot/Didot-HTF-M42-Medium.otf") format("truetype");
}
@font-face {
  font-family: "Blesing";
  src: local("Blesing"), url("/fonts/Blesing/Blesing.otf") format("truetype");
}
* {
  margin: 0;
  padding: 0;
}
body {
  height: 100vh;
}
#app {
  width: 100%;
  height: 100%;
}
.scroll-off {
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  height: 100%;
  padding-bottom: 1px;
  overflow: hidden;
}
</style>
