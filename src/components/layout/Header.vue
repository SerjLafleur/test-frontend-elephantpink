<template>
  <header>
    <div class="login">
      <img src="@/assets/lock.svg" alt="lock" />
      <p>Login</p>
    </div>
    <nav class="nav">
      <ul>
        <li>
          <a :click="setActive('home')" :class="{ active: true }">
            Home
            <Diamond class="diamond" />
          </a>
        </li>
        <li>
          <a href="#about">About</a>
        </li>
        <img src="@/assets/logo.svg" alt="logo" />
        <li><a href="#">Jewels</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
    <div class="search">
      <div class="select">
        <p>EN</p>
        <img src="@/assets/expand.svg" alt="expand" />
      </div>
      <img src="@/assets/search.svg" alt="search" />
    </div>
  </header>
</template>

<script>
import Diamond from "@/components/icons/Diamond";
export default {
  components: { Diamond },
  data() {
    return { menuActive: "home" };
  },
  methods: {
    setActive: (menuItem) => {
      this.menuActive = menuItem;
    },
    isActive: (menuItem) => {
      return this.menuActive === menuItem;
    },
  },
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");
header {
  display: flex;
  position: sticky;
  background: #fff;
  z-index: 9999;
  top: 0;
  justify-content: space-between;
  font-family: "Poppins", sans-serif;
  padding: 30px 100px 25px 100px;
  border-bottom: 1px #000 solid;
  align-items: center;
}
.login {
  display: flex;
  align-items: center;
}
.login img {
  width: 15px;
  padding-right: 5px;
}
.login p {
  font-weight: 300;
  font-size: 13px;
}
.nav img {
  width: 50px;
  padding: 0 50px;
}
.nav ul {
  margin: 0;
  padding: 0;
  list-style: none;
  display: flex;
  align-items: center;
  text-align: center;
  position: relative;
}
.nav ul li {
  min-width: 100px;
  font-weight: 200;
  text-transform: uppercase;
  font-size: 13px;
}
.nav ul li a {
  text-decoration: none;
  color: black;
  transition: all 0.4s;
  letter-spacing: 1px;
}
.nav ul li a.active {
  font-weight: 500;
}
.nav ul li a:hover {
  font-weight: 500;
}
.nav ul li .diamond {
  width: 10px;
  position: absolute;
  top: 30px;
  left: 45px;
  fill: grey;
}

.search {
  display: flex;
}
.search img {
  width: 16px;
  padding-left: 5px;
}
.select {
  display: flex;
  font-weight: 200;
  font-size: 13px;
  padding: 0 5px;
  align-items: center;
}
.select img {
  width: 12px;
  padding-left: 5px;
}
</style>