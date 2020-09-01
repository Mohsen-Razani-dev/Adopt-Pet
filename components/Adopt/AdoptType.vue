<template>
  <div class="adoptType">
    <el-container class="adoptTypeContainer">
      <el-row align="center" class="adoptTypeRow">
        <h1 class="Mainheadtxt">Adopt Types</h1>
        <el-divider></el-divider>
        <el-col :md="8" :xs="24">
          <div class="adoptTypeCenterDescrib">
            <h1 class="adoptTypeCenterDescribHeader">Choose your Adopt type</h1>
            <p class="adoptTypeCenterDescribparag">
              Lorem Ipsum is simply dummy text of the printing and typesetting
              industry. Lorem Ipsum has been the industry's standard dummy text
              ever since the 1500s, when an unknown printer took a galley of
              type and scrambled it to make a type specimen book. It has
              survived not only five centuries, but also the leap into
              electronic typesetting, remaining essentially unchanged. It was
              popularised in the 1960s with the release of Letraset sheets
              containing Lorem Ipsum passages, and more recently with desktop
              publishing software like Aldus PageMaker including versions of
              Lorem Ipsum.
            </p>
          </div>
        </el-col>
        <el-col :md="8" :sm="12">
          <div class="Type">
            <nuxt-link no-prefetch to="/Adopt/inhome" class="LinkType">
              <div id="imgType1">
                <p class="Typetxt">Adopt In Your Home</p>
              </div>
            </nuxt-link>
          </div>
        </el-col>
        <el-col :md="8" :sm="12">
          <div class="Type">
            <nuxt-link to="/Adopt/inStreet" class="LinkType">
              <div id="imgType2">
                <p class="Typetxt">Street Adopting</p>
              </div>
            </nuxt-link>
          </div>
        </el-col>
      </el-row>
    </el-container>
  </div>
</template>

<script>
import '../../assets/Styles/AdoptType.scss'
export default {
  name: 'AdoptType',
}
</script>
