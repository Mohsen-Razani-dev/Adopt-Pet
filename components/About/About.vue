<template>
  <div class="About">
    <el-main class="AboutMain">
      <el-row class="AboutRow">
        <h1>FOUNDER</h1>
        <el-col :xl="8" :md="8" class="AboutCol" v-for="F in founder">
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
          <el-col :md="4" :xs="8" v-for="i in investor" class="investorCol">
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
              <img src="../../assets/About/tehran.jpg" alt="" class="city" />
              <div class="cardDescrib">
                <h1>Tehran Office</h1>
                <span
                  >Fayazbakhsh st. Khayam Av. Imam Khomeini sq. Tehran,
                  Iran</span
                >
                <img
                  src="../../assets/About/iran-flag-icon-free-download.jpg"
                  alt="..."
                  class="flag"
                />
              </div>
            </div>
          </el-col>

          <el-col :md="8" class="officeCol">
            <div class="officeSection">
              <img src="../../assets/About/tehran.jpg" alt="" class="city" />
              <div class="cardDescrib">
                <h1>Tehran Office</h1>
                <span
                  >Fayazbakhsh st. Khayam Av. Imam Khomeini sq. Tehran,
                  Iran</span
                >
                <img
                  src="../../assets/About/iran-flag-icon-free-download.jpg"
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
        <el-col :md="8" class="footerAboutLogosCol">
          <div class="footerAboutLogosBox">
            <img src="../../assets/logopet.png" alt="" />
          </div>
        </el-col>
        <el-col :md="16" class="footerAboutLinksCol">
          <el-row>
            <el-col :md="6" class="links">
              <span class="footerAboutHeader">PRODUCT</span>
              <a class="footerAboutHeaderlink" href="#">Fetures</a>
              <a class="footerAboutHeaderlink" href="#">Sign in</a>
              <a class="footerAboutHeaderlink" href="#">Register</a>
            </el-col>
            <el-col :md="6" class="links">
              <span class="footerAboutHeader">RESOURCES</span>
              <a class="footerAboutHeaderlink" href="#">Pricing</a>
              <a class="footerAboutHeaderlink" href="#">Integration</a>
              <a class="footerAboutHeaderlink" href="#">Blog</a>
              <a class="footerAboutHeaderlink" href="#">Documentation</a>
              <a class="footerAboutHeaderlink" href="#">API Documentation</a>
            </el-col>
            <el-col :md="6" class="links">
              <span class="footerAboutHeader">COMPANY</span>
              <a class="footerAboutHeaderlink" href="#">Facebook</a>
              <a class="footerAboutHeaderlink" href="#">Google</a>
              <a class="footerAboutHeaderlink" href="#">Human Protect</a>
            </el-col>
            <el-col :md="6" class="links">
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
export default {
  name: 'About',
  data: () => ({
    founder: [
      {
        id: 1,
        name: 'Mohsen Razani',
        img: require('../../assets/About/man.jpg'),
        role: 'Founder',
        quotation:
          "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
      },
      {
        id: 2,
        name: 'Mohsen Razani',
        img: require('../../assets/About/man.jpg'),
        role: 'Founder',
        quotation:
          "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
      },
      {
        id: 3,
        name: 'Mohsen Razani',
        img: require('../../assets/About/man.jpg'),
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
        img: require('../../assets/About/investor/1200px-Google__G__Logo.svg.png'),
      },
      {
        id: 2,
        name: 'Google Health',
        link: 'https://google.com',
        img: require('../../assets/About/investor/1200px-Seal_of_the_Department_of_Environment_and_Natural_Resources.svg.png'),
      },
      {
        id: 3,
        name: 'Google Health',
        link: 'https://google.com',
        img: require('../../assets/About/investor/ehscebzgx2cvshmw9vxb.jpg'),
      },
      {
        id: 4,
        name: 'Google Health',
        link: 'https://google.com',
        img: require('../../assets/About/investor/netflix-logo-png-2562.png'),
      },
      {
        id: 5,
        name: 'Google Health',
        link: 'https://google.com',
        img: require('../../assets/About/investor/un_PNG20.png'),
      },
    ],
  }),
}
</script>

<style scoped lang="scss">
.About {
  width: 100%;
  min-height: 100vh;
  height: 100%;
  padding: 100px 4% 0 4%;
  .AboutMain {
    height: 100%;
    width: 100%;
    background-color: #f5f7fb;
    padding: 6%;
    .AboutRow {
      .AboutCol {
        padding: 30px;
        .section {
          text-align: center;
          background-color: white;
          border-radius: 7px;
          padding: 30px;
          height: 440px;
          display: grid;
          justify-content: center;
          justify-items: center;
          align-items: center;
          align-content: center;
          align-self: center;
          box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.36);
          img {
            height: 90px;
            width: 90px;
            border-radius: 100%;
            object-fit: cover;
          }
          h1 {
            font-family: Gilroy-Medium;
            font-size: 23px;
            margin: 20px 0 3px 0;
            color: #2d4050;
          }
          h2 {
            font-family: Gilroy-Medium;
            font-size: 19px;
            margin: 0 0 15px 0;
            color: #babfc6;
          }
          i {
            cursor: pointer;
            font-size: 24px;
            margin-bottom: 10px;
            color: #37a0f7;
          }
          p {
            font-size: 15px;
            color: rgba(112, 116, 122, 0.99);
          }
        }
      }
    }
  }
  .investor {
    padding: 100px 0;
    text-align: center;
    .investorRow {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-wrap: wrap;
      .investorCol {
        padding: 10px;
        .investorBox {
          padding: 40px;
          min-height: 200px;
          height: 100%;
          display: flex;
          align-items: center;
          justify-content: center;
          border-radius: 8px;
          box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.36);
          img {
            width: 100%;
          }
        }
      }
    }
  }

  .office {
    background-color: #f5f7fb;
    .officeMain {
      .officeRow {
        display: flex;
        justify-content: center;
        .officeCol {
          padding: 30px;
          .officeSection {
            background-color: white;
            padding: 0 0 30px 0;
            display: grid;
            text-align: center;
            align-content: center;
            justify-items: center;
            border-radius: 7px;
            box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.26);
            .city {
              width: 100%;
              height: 200px;
              object-fit: cover;
              border-top-left-radius: 7px;
              border-top-right-radius: 7px;
              margin-bottom: 40px;
            }
            .cardDescrib {
              min-height: 250px;
              display: grid;
              text-align: center;
              align-content: center;
              justify-items: center;
              h1 {
                font-size: 26px;
                margin-bottom: 30px;
                color: #394a58;
                font-family: Gilroy-Bold;
              }
              span {
                font-family: Gilroy-Medium;
                font-size: 20px;
                padding: 0 55px 40px 55px;
                color: #b2b8c0;
              }
              .flag {
                text-align: center;
                height: 20px;
                width: 30px;
              }
            }
          }
        }
      }
    }
  }
  .footer{
    background-color: white;
    padding: 80px 40px 30px 40px;
    .footerAboutLogosCol{
      .footerAboutLogosBox{
        img{
          height: 200px;
          width: 200px;
        }
      }
    }
    .footerAboutLinksCol{
      .links{
        display: grid;
        padding: 0 20px;
        .footerAboutHeader{
          color: #40a6f0;
          font-size: 17px;
          margin-bottom: 30px;
        }
        .footerAboutHeaderlink{
          color: #a5adb4;
          font-size: 14px;
          text-decoration: none;
        }
      }
    }
  }
}
</style>
