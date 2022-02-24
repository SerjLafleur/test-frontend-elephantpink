<template>
  <section>
    <div>
      <h2 class="line"><span>Our Collection</span></h2>
      <div class="line-text">
        <p>
          Specially crafted with the utmost of precision and care, our dreamy
          jewels are meant yo make your wishes come true
        </p>
      </div>
    </div>
    <div class="card">
      <div
        v-for="product in products.slice(0, showmore ? 6 : 3)"
        :key="product.id"
      >
        <Card :product="product" />
      </div>
    </div>
    <div class="button">
      <Button
        title="View All"
        :class="{ toggle: showMore }"
        @click="toggle"
      ></Button>
    </div>
  </section>
</template>

<script>
import Card from "@/components/collections/Card";
import Button from "@/components/button/Button";
export default {
  components: { Card, Button },
  data() {
    return {
      showmore: false,
      products: [
        {
          id: 1,
          src: "https://sergiobaltanas.com/wp-content/uploads/2022/02/ring.jpg",
          title: "Diamond 1",
          text: "The shining diamonds of the bracelet sprinkle the space.",
        },
        {
          id: 2,
          src: "https://sergiobaltanas.com/wp-content/uploads/2022/02/ring.jpg",
          title: "Diamond 2",
          text: "The instrinsic beauty lies in these sleek and clean earrings where polished diamond embrace the wearer and mark the shape of the face.",
        },
        {
          id: 3,
          src: "https://sergiobaltanas.com/wp-content/uploads/2022/02/ring.jpg",
          title: "Diamond 3",
          text: "The sparkle of the diamonds on this powerful ring symbolize the strength of beauty.",
        },
        {
          id: 4,
          src: "https://sergiobaltanas.com/wp-content/uploads/2022/02/ring.jpg",
          title: "Diamond 4",
          text: "The instrinsic beauty lies in these sleek and clean earrings where polished diamond embrace the wearer and mark the shape of the face.",
        },
        {
          id: 5,
          src: "https://sergiobaltanas.com/wp-content/uploads/2022/02/ring.jpg",
          title: "Diamond 4",
          text: "The sparkle of the diamonds on this powerful ring symbolize the strength of beauty.",
        },
        {
          id: 6,
          src: "https://sergiobaltanas.com/wp-content/uploads/2022/02/ring.jpg",
          title: "Diamond 6",
          text: "The shining diamonds of the bracelet sprinkle the space.",
        },
      ],
    };
  },
  methods: {
    toggle() {
      console.log("olaaaa");
      this.showmore = !this.showmore;
    },
  },
};
</script>

<style lang="scss" scoped>
h2 {
  font-family: "Didot", sans-serif;
  font-size: 25px;
  margin: 80px 100px 40px 100px;
  text-align: center;
  text-transform: uppercase;
}
h2.line {
  position: relative;
  z-index: 1;
}
h2.line:before {
  border-top: 1px solid grayscale($color: #d2d2d2);
  content: "";
  margin: 0 auto;
  position: absolute;
  top: 50%;
  left: 0;
  right: 0;
  bottom: 0;
  width: 95%;
  z-index: -1;
}
h2.line span {
  background: #fff;
  padding: 0 15px;
}
.line-text {
  text-align: center;
  font-family: "Poppins", sans-serif;
  font-size: 11px;
  letter-spacing: 1px;
  width: 40%;
  margin: 0 auto 100px auto;
}
.card {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  justify-content: center;
  justify-items: center;
  margin: 0 100px;
}
.button {
  margin: 100px 0;
  display: flex;
  justify-content: center;
}
</style>