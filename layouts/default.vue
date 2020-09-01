<template>
  <div>
    <DesktopNavbar />
    <MobileNavbar />
    <Nuxt />
  </div>
</template>

<script>
import MobileNavbar from '~/components/Navbar/MobileNavbar'
import DesktopNavbar from '~/components/Navbar/DesktopNavbar'
export default {
  components: {
    DesktopNavbar,
    MobileNavbar,
  },
  computed: {
    isSidebar() {
      return this.$store.getters['nav/toggleSidebar']
    },
  },
  watch: {
    $route: function () {
      if (process.client && this.isSidebar && window.innerWidth < 768) {
        this.$store.dispatch('nav/toggleSidebar')
      }
    },
  },
}
</script>
<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
</style>
