<template>
  <div class="container">
    <img :src="product.src" :alt="product.title" />
    <h3>{{ product.title }}</h3>
    <hr />
    <p>{{ product.text }}</p>
    <diamond />
  </div>
</template>

<script>
import Diamond from "@/components/icons/Diamond";
export default {
  props: ["product"],
  components: { Diamond },
};
</script>

<style lang="scss" scoped>
.container {
  width: 350px;
  height: 550px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  box-shadow: 1px 5px 10px 10px rgba(208, 208, 208, 0.2);
}
.container img {
  width: 180px;
}
.container h3 {
  font-family: "Didot", sans-serif;
  text-transform: uppercase;
  font-size: 18px;
  letter-spacing: 1px;
  margin: 30px 0;
}
.container hr {
  height: 1px;
  background-color: #ddd;
  width: 170px;
  border: none;
}
.container p {
  font-family: "Poppins", sans-serif;
  font-size: 10px;
  color: #c6c6c6;
  width: 240px;
  text-align: center;
  margin: 30px 0 50px 0;
}
</style>