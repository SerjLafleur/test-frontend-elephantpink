<template>
  <main>
    <carousel>
      <carousel-slide
        v-for="slide in slides"
        :key="slide.src"
        class="carousel-slider"
      >
        <div class="text-carousel">
          <h1 class="title">{{ slide.title }}</h1>
          <hr class="divider" />
          <p class="text">{{ slide.text }}</p>
        </div>
        <img :src="slide.src" :alt="slide.alt" />
      </carousel-slide>
      <div class="stepper-slider">
        <!-- <div
          v-for="slide in slides"
          :key="slide.src"
          class="step-slider-button"
          :class="{ active: slide.id === currentSlide }"
        >
          <Diamond class="diamond" />
        </div> -->
      </div>
    </carousel>
  </main>
</template>

<script>
import Diamond from "@/components/icons/Diamond";
import Carousel from "./Carousel.vue";
import CarouselSlide from "./CarouselSlide.vue";

export default {
  components: { Carousel, CarouselSlide, Diamond },
  data() {
    return {
      currentStep: "slider1",
      slides: [
        {
          id: "slider1",
          src: "https://sergiobaltanas.com/wp-content/uploads/2022/02/slider1.jpg",
          alt: "slider 1",
          title: "Diamonds",
          text: "Diamons are the brightest stars and only the sky is the limit when it comes to achieving our jewels",
        },
        {
          id: "slider2",
          src: "https://sergiobaltanas.com/wp-content/uploads/2022/02/slider2.png",
          alt: "slider 2",
          title: "New Diamonds",
          text: "Encuentra las joyas que van con tu estilo, inspírate y completa tu look con nuestras creaciones.",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.carousel {
  position: relative;
  overflow: hidden;
  width: 100%;
  height: 650px;
  z-index: 10;
}
.carousel-slider {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  display: grid;
  align-items: center;
  justify-items: center;
}
.carousel-slider img {
  width: 100%;
  height: 650px;
  object-fit: cover;
  filter: brightness(0.4);
}
.text-carousel {
  position: absolute;
  width: 30%;
  z-index: 2;
  top: 200px;
}
.title {
  color: #fff;
  font-size: 35px;
  text-transform: uppercase;
  font-family: "Didot", sans-serif;
  text-align: center;
  letter-spacing: 3px;
}
.divider {
  margin: 30px 50px;
}
.text {
  color: white;
  font-family: "Poppins", sans-serif;
  font-size: 11px;
  font-weight: 300;
  color: grayscale($color: #dbdbdb);
  text-align: center;
  letter-spacing: 1px;
}
.stepper-slider {
  z-index: 20;
  width: 100px;
  text-align: center;
  height: 40px;
  position: absolute;
  bottom: 80px;
  display: grid;
  align-items: center;
  justify-items: center;
  grid-template-columns: 1fr 1fr;
  justify-content: space-around;
  right: 50%;
  margin-right: -50px;
}
</style>