<template>
  <button class="component-button">{{ title }}</button>
</template>

<script>
export default {
  props: ["title"],
};
</script>

<style lang="scss">
.component-button {
  font-family: "Poppins", sans-serif;
  text-transform: uppercase;
  border: 1px solid #000;
  padding: 13px 0;
  width: 200px;
  letter-spacing: 2px;
  outline: none;
  background-color: white;
  cursor: pointer;
  -webkit-transition-duration: 0.4s;
  transition-duration: 0.4s;
}
.component-button:hover {
  background-color: #000;
  color: white;
}
</style>