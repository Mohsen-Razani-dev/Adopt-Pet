<template>
  <div id="nav" class="nav">
    <div class="navbrand">
      <nuxt-link to="/" class="brand">
        <img class="logo" src="../assets/logopet.png" alt="" />
      </nuxt-link>
    </div>
    <nav class="navlinks">
      <nuxt-link to="/">Home</nuxt-link>
      <nuxt-link to="/Adopt">Adopt</nuxt-link>
      <nuxt-link to="/Clinic">Clinic</nuxt-link>
      <nuxt-link to="/Blog">Blog</nuxt-link>
      <nuxt-link to="/About-Us">About Us</nuxt-link>
    </nav>
    <div class="help">
      <button>HELP</button>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Navbar',
  mounted() {
    this.$nextTick(function () {
      window.addEventListener('scroll', function () {
        const navbar = document.getElementById('nav')
        const navClasses = navbar.classList
        if (document.documentElement.scrollTop >= 50) {
          if (navClasses.contains('shrink') === false) {
            navClasses.toggle('shrink')
          }
        } else if (navClasses.contains('shrink') === true) {
          navClasses.toggle('shrink')
        }
      })
    })
  },
}
</script>
<style scoped lang="scss">
* {
  padding: 0;
  margin: 0;
}
.shrink {
  background: #e8eefa;
  transition: 500ms all ease-out;
}
.nav {
  transition: 500ms all ease-out;
  z-index: 10000;
  position: fixed;
  top: 0;
  padding: 16px 8%;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  @font-face {
    font-family: 'Gilroy-Medium' !important;
  }
  .help {
    button {
      background-color: #0b4d7a;
      color: rgb(255, 255, 255);
      border: none;
      font-size: 17px;
      padding: 12px 30px;
      border-radius: 30px;
      box-shadow: 0 0 10px 0 rgba(53, 96, 131, 0.51);
    }
  }
  .navbrand {
    height: 50px;
    width: 50px;
    img {
      height: 100%;
      width: 100%;
    }
  }
  .navlinks {
    a {
      color: #0b4d7a;
      padding: 0 20px;
      text-decoration: none;
      font-size: 19px;
      /* stylelint-disable */
      font-family: 'Gilroy-Bold' !important;
      /* stylelint-enable */
    }
  }
}
.change_color {
  background-color: red;
}
</style>
