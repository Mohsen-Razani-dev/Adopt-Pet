<template>
  <header id="nav" class="nav">

    <div class="brand-name">
      <nuxt-link to="/">
        <img src="../../assets/Images/logopet.png" alt="" class="brand-img">
      </nuxt-link>
    </div>

    <div class="drawer-toggle" role="button" @click="$store.dispatch('nav/toggleSidebar')">
      <fa icon="align-left"  style="font-size: 40px;color: #0b4d7a"/>
    </div>
    <div class="app-links">
      <AppLink></AppLink>
    </div>
    <div class="help">
      <nuxt-link to="/">
        <button class="helpButton">Help !</button>
      </nuxt-link>
    </div>
  </header>
</template>

<script>
  import AppLink from '~/components/Navbar/AppLinks'
  export default {
    components: { AppLink },
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
  .nav{
    transition: 500ms all ease-out;
    z-index: 1000;
    position: fixed;
    top: 0;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-around;
    padding: 20px 0;
    @font-face {
      font-family: 'Gilroy-Medium' !important;
    }
  }
  .shrink{
    background: #e8eefa;
    transition: 500ms all ease-out;
  }
  .app-links{
    justify-self: end;
  }
  .brand-name {
    font-size: 1.3rem;
    height: 100%;
    display: flex;
    align-items: center;
  }
  .help{
    .helpButton{
      border: none;
      border-radius: 35px;
      background-color: #0b4d7a;
      color: white;
      font-size: 16px;
      padding: 10px 20px;
      font-family: Gilroy-Medium;
    }
  }
  .brand-name a {
    text-decoration: none;
    color: white;
    margin: 0;
    display: flex;
    align-items: center;
  }
  .brand-img{
    height: 60px;
    width: 60px;
    padding: 5px;
  }
  .drawer-toggle {
    display: flex;
    justify-self: end;
    flex-direction: column;
    justify-content: space-around;
    height: 50%;
    width: 35px;
    padding-right: 16px;
    cursor: pointer;
    box-sizing: content-box;
  }
  @media (max-width: 767px) {
    .help{
      display: none;
    }
    .nav{
      width: 100% !important;
      justify-content: space-between;
    }
    .app-links {
      display: none;
    }
    .brand-name{
      padding-left: 50px;
    }
    .drawer-toggle{
      padding-right: 50px;
    }
  }
  @media (min-width: 768px) {
    .app-links {
      display: block;
    }
    .drawer-toggle {
      display: none;
    }
  }
</style>
