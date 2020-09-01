<template>
  <div class="About">
    <el-main class="AboutMain">
      <el-row class="AboutRow">
        <h1>FOUNDER</h1>
        <el-col :xl="8" :md="8" :sm="12" class="AboutCol" v-for="F in founder">
          <div class="section">
            <img :src="F.img" alt="" />
            <h1>{{ F.name }}</h1>
            <h2>{{ F.role }}</h2>
            <i class="el-icon-s-promotion"></i>
            <p>
              {{ F.quotation }}
            </p>
          </div>
        </el-col>
      </el-row>
    </el-main>
    <div class="investor">
      <h1>INVESTOR</h1>
      <el-main>
        <el-row class="investorRow">
          <el-col :md="4" :sm="8" v-for="i in investor" class="investorCol">
            <div class="investorBox">
              <img :src="i.img" alt="..." />
            </div>
          </el-col>
        </el-row>
      </el-main>
    </div>

    <div class="office">
      <el-main class="officeMain">
        <el-row class="officeRow">
          <el-col :md="8" class="officeCol">
            <div class="officeSection">
              <img
                src="../../assets/Images/About/tehran.jpg"
                alt=""
                class="city"
              />
              <div class="cardDescrib">
                <h1>Tehran Office</h1>
                <span
                  >Fayazbakhsh st. Khayam Av. Imam Khomeini sq. Tehran,
                  Iran</span
                >
                <img
                  src="../../assets/Images/About/iran-flag-icon-free-download.jpg"
                  alt="..."
                  class="flag"
                />
              </div>
            </div>
          </el-col>

          <el-col :md="8" class="officeCol">
            <div class="officeSection">
              <img
                src="../../assets/Images/About/tehran.jpg"
                alt=""
                class="city"
              />
              <div class="cardDescrib">
                <h1>Tehran Office</h1>
                <span
                  >Fayazbakhsh st. Khayam Av. Imam Khomeini sq. Tehran,
                  Iran</span
                >
                <img
                  src="../../assets/Images/About/iran-flag-icon-free-download.jpg"
                  alt="..."
                  class="flag"
                />
              </div>
            </div>
          </el-col>
        </el-row>
      </el-main>
    </div>
    <footer class="footer">
      <el-row>
        <el-col :lg="6" :md="8" :sm="0" :xs="0" class="footerAboutLogosCol">
          <div class="footerAboutLogosBox">
            <img src="../../assets/Images/logopet.png" alt="" />
          </div>
        </el-col>
        <el-col :lg="18" :md="16" :sm="20" :xs="24" class="footerAboutLinksCol">
          <el-row>
            <el-col :md="6" :sm="6" class="links">
              <span class="footerAboutHeader">PRODUCT</span>
              <a class="footerAboutHeaderlink" href="#">Fetures</a>
              <a class="footerAboutHeaderlink" href="#">Sign in</a>
              <a class="footerAboutHeaderlink" href="#">Register</a>
            </el-col>
            <el-col :md="6" :sm="6" class="links">
              <span class="footerAboutHeader">RESOURCES</span>
              <a class="footerAboutHeaderlink" href="#">Pricing</a>
              <a class="footerAboutHeaderlink" href="#">Integration</a>
              <a class="footerAboutHeaderlink" href="#">Blog</a>
              <a class="footerAboutHeaderlink" href="#">Documentation</a>
              <a class="footerAboutHeaderlink" href="#">API Documentation</a>
            </el-col>
            <el-col :md="6" :sm="6" class="links">
              <span class="footerAboutHeader">COMPANY</span>
              <a class="footerAboutHeaderlink" href="#">Facebook</a>
              <a class="footerAboutHeaderlink" href="#">Google</a>
              <a class="footerAboutHeaderlink" href="#">Human Protect</a>
            </el-col>
            <el-col :md="6" :sm="6" class="links">
              <span class="footerAboutHeader">LEGAL</span>
              <a class="footerAboutHeaderlink" href="#">Privacy Policy</a>
              <a class="footerAboutHeaderlink" href="#">Terms</a>
            </el-col>
          </el-row>
        </el-col>
      </el-row>
    </footer>
  </div>
</template>

<script>
import '../../assets/Styles/About.scss'
export default {
  name: 'About',
  data: () => ({
    founder: [
      {
        id: 1,
        name: 'Mohsen Razani',
        img: require('../../assets/Images/About/man.jpg'),
        role: 'Founder',
        quotation:
          "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
      },
      {
        id: 2,
        name: 'Mohsen Razani',
        img: require('../../assets/Images/About/man.jpg'),
        role: 'Founder',
        quotation:
          "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
      },
      {
        id: 3,
        name: 'Mohsen Razani',
        img: require('../../assets/Images/About/man.jpg'),
        role: 'Founder',
        quotation:
          "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
      },
    ],
    investor: [
      {
        id: 1,
        name: 'Google Health',
        link: 'https://google.com',
        img: require('../../assets/Images/About/investor/1200px-Google__G__Logo.svg.png'),
      },
      {
        id: 2,
        name: 'Google Health',
        link: 'https://google.com',
        img: require('../../assets/Images/About/investor/1200px-Seal_of_the_Department_of_Environment_and_Natural_Resources.svg.png'),
      },
      {
        id: 3,
        name: 'Google Health',
        link: 'https://google.com',
        img: require('../../assets/Images/About/investor/ehscebzgx2cvshmw9vxb.jpg'),
      },
      {
        id: 4,
        name: 'Google Health',
        link: 'https://google.com',
        img: require('../../assets/Images/About/investor/netflix-logo-png-2562.png'),
      },
      {
        id: 5,
        name: 'Google Health',
        link: 'https://google.com',
        img: require('../../assets/Images/About/investor/un_PNG20.png'),
      },
    ],
  }),
}
</script>
