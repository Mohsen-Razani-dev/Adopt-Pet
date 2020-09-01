<template>
  <ul class="nav-list">
    <h1 class="sideHeaderTxt">ADPET</h1>
    <el-input
      class="searchbar"
      placeholder="Pick a date"
      suffix-icon="el-icon-search"
      v-model="input1">
    </el-input>
    <li class="nav-item"><nuxt-link to="/">Home</nuxt-link></li>
    <li class="nav-item"><nuxt-link to="/adopt">Adopt</nuxt-link></li>
    <li class="nav-item"><nuxt-link to="/clinic">Clinic</nuxt-link></li>
    <li class="nav-item"><nuxt-link to="/blog">Blog</nuxt-link></li>
    <li class="nav-item"><nuxt-link to="/about-us">AboutUs</nuxt-link></li>
  </ul>
</template>
<script>
export default {
  name: 'AppLink',
}
</script>
<style scoped lang="scss">
.nav-list {
  list-style: none;
  padding: 0;
  margin: 0;
}
.nav-item {
  a{
    color: #0b4d7a;
    padding: 0 20px;
    text-decoration: none;
    font-size: 17px;
    /* stylelint-disable */
    font-family: 'Gilroy-Bold' !important;
    /* stylelint-enable */
    &:hover{
      color: #2a86c4;
    }
    &:active{
      color: #41a4e7;
    }
  }
}
@media (max-width: 767px) {
  .nav-list {
    display: block;
  }
  .searchbar{
    display: block;
  }
  .nav-item {
    margin-top: 10px;
    margin-bottom: 18px;
    padding: 6px;
    a{
      padding: 0 10px;
      font-size: 14px;
    }
  }
  .sideHeaderTxt{
    font-size: 25px;
    color: #0b4d7a;
    font-family: Gilroy-Medium;
    margin-bottom: 40px;
  }
}
@media (min-width: 768px) {
  .nav-list {
    display: flex;
  }
  .searchbar{
    display: none;
  }
  .sideHeaderTxt{
    display: none;
  }
}
</style>
