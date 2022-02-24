<template>
  <div class="carousel">
    <slot></slot>

    <button @click.prevent="next" class="btn btn-next">
      <img src="@/assets/arrow.svg" />
    </button>
    <button @click.prevent="prev" class="btn btn-prev">
      <img class="img-prev" src="@/assets/arrow.svg" />
    </button>
  </div>
</template>


<script>
export default {
  data() {
    return {
      index: 0,
      slides: [],
      slideActive: 0,
      slideDirection: "",
    };
  },
  computed: {
    slidesLength() {
      return this.slides.length;
    },
  },
  mounted() {
    this.slides = this.$children;
    this.slides.map((slide, index) => {
      slide.index = index;
    });
  },
  methods: {
    next() {
      this.index++;
      if (this.index >= this.slidesLength) {
        this.index = 0;
      }
      this.slideDirection = "slide-right";
    },
    prev() {
      this.index--;
      if (this.index < 0) {
        this.index = this.slidesLength - 1;
      }
      this.slideDirection = "slide-left";
    },
  },
};
</script>

<style lang="scss" scoped>
.btn {
  padding: 5px 10px;
  background-color: transparent;
  border: 1px solid transparent;
  margin: 5px 10px;
  color: #fff;
  height: 50px;
  width: 50px;
  position: absolute;
  margin-top: -25px;
  z-index: 2;
}
.btn:hover {
  cursor: pointer;
}
.btn:focus {
  outline: none;
}
.btn-next {
  top: calc(50% - 20px);
  right: 100px;
}
.btn-prev {
  top: calc(50% - 20px);
  left: 100px;
}
.img-prev {
  transform: rotate(180deg);
}
</style>