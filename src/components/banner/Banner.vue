<template>
  <section>
    <div class="banner-title">
      <h2>
        Contact Us
        <span>Diamonds</span>
      </h2>
    </div>
    <div class="banner-text">
      <p>
        Sed ut perspiciaties unde omnis iste natus error sit voluptatem
        accusantium doloremque laudantium, totam rem apreriam. eaque ipsa quae
        ab illo inventore.
      </p>
    </div>
    <div class="banner-button">
      <Button :title="title"></Button>
    </div>
  </section>
</template>

<script>
import Button from "@/components/button/Button";
export default {
  components: { Button },
  data() {
    return {
      title: "Contact",
    };
  },
};
</script>


<style lang="scss" scoped>
section {
  margin: 0 120px 100px 120px;
  padding: 15px 0;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  justify-items: center;
  align-items: center;
  box-shadow: 1px 10px 10px 5px rgba(208, 208, 208, 0.2);
}
.banner-title h2 {
  font-size: 18px;
  font-weight: 500;
  margin-left: 0;
  font-family: "Poppins", sans-serif;
  color: #c0984f;
  letter-spacing: 1px;
  text-transform: uppercase;
}
.banner-title span {
  font-family: "Blesing", sans-serif;
  font-size: 7px;
}
.banner-text {
  font-size: 9px;
  color: #c6c6c6;
  font-family: "Poppins", sans-serif;
}
</style>