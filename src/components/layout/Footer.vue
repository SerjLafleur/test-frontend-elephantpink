<template>
  <footer>
    <nav class="footer-nav">
      <ul>
        <li><a href="#">Services</a></li>
        <div class="vl">|</div>
        <li><a href="#">Privacy and Cookie Policy</a></li>
      </ul>
    </nav>
    <div>
      <Logo class="footer-logo" />
    </div>
    <div class="social">
      <img src="@/assets/social-facebook.svg" alt="social-facebook" />
      <img src="@/assets/social-twitter.svg" alt="social-twitter" />
    </div>
  </footer>
</template>

<script>
import Logo from "@/components/icons/Logo";
export default {
  components: { Logo },
};
</script>

<style lang="scss" scoped>
footer {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  font-family: "Poppins", sans-serif;
  justify-items: center;
  padding: 30px 0 25px 0;
  background-color: black;
  align-items: center;
}
.footer-nav ul {
  margin: 0;
  padding: 0;
  list-style: none;
  display: flex;
  align-items: center;
}
.footer-nav li {
  padding: 0 15px;
}
.footer-nav ul li a {
  text-decoration: none;
  color: white;
  transition: all 0.4s;
  font-size: 12px;
  font-weight: 400;
  text-decoration: underline;
}
.vl {
  border-left: 1px solid white;
  height: 30px;
}
.footer-logo {
  width: 50px;
}
.social {
  display: flex;
  margin-left: 150px;
}
.social img {
  width: 20px;
  height: 20px;
  padding: 0 5px;
}
</style>