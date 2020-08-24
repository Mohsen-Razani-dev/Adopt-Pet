<template>
  <div>
    <div class="homepageheader">
      <el-container class="homepageContainer">
        <el-row class="homepageRow">
          <el-col :md="15" class="homepageCol">
            <div class="homepageDescr">
              <h1>
                Move The World <br />
                For Animals
              </h1>
              <h4>
                Billion of animals are suffering right now. When did our world
                become so cruel? Does the life of an animal mean nothing at all?
                Join us to end animal cruelty .
              </h4>
              <button>Join Us</button>
            </div>
          </el-col>
          <el-col :md="9" class="homepageCol">
            <div class="homepageSignUp">
              <div class="signup">
                <HomepageJoin />
              </div>
            </div>
          </el-col>
        </el-row>
      </el-container>
    </div>
    <div class="homepageSection">
      <el-container class="homepageSectionContainer">
        <el-row class="nameofPlan">
          <h1>
            if you dont know what is this plan you can see tutorial
            <a href="#" class="tutorialVid">&nbsp;Tour</a>
          </h1>
        </el-row>
        <el-row>
          <el-col :md="8">
            <div class="sectionpart">
              <img src="../../assets/HomePage/Vectors/001-plant.png" alt="" />
              <h1 class="sectionpartTitle">Planting an idea</h1>
              <span class="sectionpartDescr"
                >lorem ipsum Vivamus magna justo so this Car is Shadowblade
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. It has survived not only five centuries, but also the
                leap into electronic typesetting, remaining essentially
                unchanged.</span
              >
            </div>
          </el-col>
          <el-col :md="8">
            <div class="sectionpart">
              <img src="../../assets/HomePage/Vectors/002-green.png" alt="" />
              <h1 class="sectionpartTitle">Develop your ideas</h1>
              <span class="sectionpartDescr"
                >lorem ipsum Vivamus magna justo so this Car is Shadowblade
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. It has survived not only five centuries, but also the
                leap into electronic typesetting, remaining essentially
                unchanged.</span
              >
            </div>
          </el-col>
          <el-col :md="8">
            <div class="sectionpart">
              <img src="../../assets/HomePage/Vectors/003-modern.png" alt="" />
              <h1 class="sectionpartTitle">See it in real world</h1>
              <span class="sectionpartDescr"
                >lorem ipsum Vivamus magna justo so this Car is Shadowblade
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. It has survived not only five centuries, but also the
                leap into electronic typesetting, remaining essentially
                unchanged.</span
              >
            </div>
          </el-col>
        </el-row>
      </el-container>
    </div>
    <div class="homepageSecDescr">
      <el-container class="homepageSectionDescr">
        <el-row>
          <el-col :md="14" class="homepageSectionDescrColVideo">
            <youtube
              class="youtube"
              :player-vars="{ autoplay: 0 }"
              video-id="tY-6MLpJSqY"
            />
          </el-col>
          <el-col :md="10" class="homepageSectionDescrColDet">
            <h1 class="homepageSectionDescrColDeth1">
              We share the best ideas for everyone to watch
            </h1>
            <p class="homepageSectionDescrColDetp">
              The standard chunk of Lorem Ipsum used since the 1500s is
              reproduced below for those interested. Sections 1.10.32 and
              1.10.33 from "de Finibus Bonorum et Malorum" by Cicero are also
              reproduced in their exact original form, accompanied by English
              versions from the 1914 translation by H. Rackham. There are many
              variations of passages of Lorem Ipsum available, but the majority
              have suffered alteration in some form, by injected humour, or
              randomised words which don't look even slightly believable.
            </p>
            <button class="homepageSectionDescrColDetbutton">More</button>
          </el-col>
        </el-row>
      </el-container>
    </div>
    <div class="topplusfooter">
      <el-container class="topplusfootercontainer">
        <el-row class="topplusfooterrow">
          <el-col :md="12" class="topplusfootercol">
            <img
              src="../../assets/HomePage/Vectors/004-earth-day.png"
              alt="..."
              class="topplusfootercolimg"
            />
            <span class="topplusfootercolspan"
              >randomised words which don't look even slightly believable</span
            >
            <p class="topplusfootercolp">
              The standard chunk of Lorem Ipsum used since <br />
              the 1500s is reproduced below for those interested. Sections
              1.10.32 and 1.10.33 from "de Finibus Bonorum et Malorum" <br />
              by Cicero are
            </p>
          </el-col>
        </el-row>
      </el-container>
    </div>
    <div class="mainfooter">
      <el-container class="mainfootercontainer">
        <el-row class="mainfooterrow">
          <el-col :xl="18" :md="18" class="mainfootercollinks">
            <el-row>
              <el-col :md="6" class="footerlinks">
                <span class="footerheadlink">Product</span>
                <a class="footerlink" href="#">Fetures</a>
                <a class="footerlink" href="#">Sign in</a>
                <a class="footerlink" href="#">Register</a>
              </el-col>
              <el-col :xl="6" :md="6" class="footerlinks">
                <span class="footerheadlink">About us</span>
                <a class="footerlink" href="#">API</a>
                <a class="footerlink" href="#">Document</a>
                <a class="footerlink" href="#">Blog</a>
              </el-col>
              <el-col :xl="6" :md="6" class="footerlinks">
                <span class="footerheadlink">Social Media</span>
                <a class="footerlink" href="#">Facebook</a>
                <a class="footerlink" href="#">Twitter</a>
                <a class="footerlink" href="#">Linkdin</a>
              </el-col>
              <el-col :xl="6" :md="6" class="footerlinks">
                <span class="footerheadlink">Contact us</span>
                <a class="footerlink" href="#">mohsenrazani.z@gmail.com</a>
                <a class="footerlink" href="#">+989212196508</a>
                <a class="footerlink" href="#">Iran - Tehran</a>
              </el-col>
            </el-row>
          </el-col>
          <el-col :xl="6" :md="6" class="mainfootercollogo">
            <img
              class="mainfooterlogo"
              src="../../assets/logopet.png"
              alt="..."
            />
          </el-col>
          <el-col :xl="24" :md="24" class="copyrightcol">
            <p class="copyright">
              Copyright © 2020 Mohsen Razani. All right Reserved
            </p>
          </el-col>
        </el-row>
      </el-container>
    </div>
  </div>
</template>
<script>
import HomepageJoin from '~/components/HomePage/Signupform'
export default {
  name: 'HomePage',
  components: { HomepageJoin },
  data: () => ({}),
}
</script>
<style lang="scss">
body {
  margin: 0;
}
.homepageheader {
  display: flex;
  align-items: center;
  height: 100%;
  min-height: 100vh;
  background-image: url('../../assets/HomePage/mainbg.png');
  background-position: right;
  background-size: cover;
  background-repeat: no-repeat;
  .homepageContainer {
    padding: 0 8%;
    .homepageRow {
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
      .homepageCol {
        padding: 80px 50px 50px 50px;
        .signup {
          //border: 1px solid white;
          background-color: rgba(255, 255, 255, 0.28);
          backdrop-filter: blur(4px);
          padding: 25px 25px 10px 25px;
          border-radius: 22px;
          box-shadow: 0 0 9px 0 rgba(0, 0, 0, 0.3);
          .signupbrand {
            font-size: 30px;
            width: 100%;
            padding: 0 0 10px 0;
            text-align: center;
            display: flex;
            justify-content: center;
            color: #af4448;
            /* stylelint-disable */
            font-family: 'Gilroy-Heavy' !important;
            /* stylelint-enable */
          }
          .form {
            .haveAcc {
              display: flex;
              align-items: center;
              justify-content: center;
              margin-top: 10px;
              font-size: 14px;
              color: #4d2c58;
              a {
                text-decoration: none;
                font-size: 15px;
                outline: none;
                color: rgba(108, 61, 124, 0.92);
              }
            }
            .signupButton {
              width: 100%;
              background-color: rgba(155, 81, 224, 0.82) !important;
              border-radius: 50px !important;
            }
            .signupButton:disabled,
            .signupButton[disabled] {
              background-color: rgba(175, 126, 221, 0.82) !important;
              color: rgba(231, 230, 230, 0.87) !important;
            }
            .FollowUs {
              margin-top: 40px;
              display: flex;
              width: 100%;
              justify-content: space-between;
              .FollowUsBtn {
                height: 50px;
                width: 50px;
                border-radius: 50%;
                display: flex;
                align-items: center;
                justify-content: center;
                background-color: rgba(155, 81, 224, 0.08);
                color: #9b51e0;
                font-size: 21px;
                &:hover {
                  background-color: #9b51e0;
                  color: white;
                }
              }
            }
            .checkbox {
              margin-bottom: 5px;
            }
          }
        }
        .homepageDescr {
          text-align: center;
          padding-top: 40px;
          h1 {
            font-size: 50px;
            font-weight: 900;
            color: #355f81;
            margin-bottom: 20px;
            /* stylelint-disable */
            font-family: 'Gilroy-Heavy' !important;
            /* stylelint-enable */
          }
          h4 {
            font-size: 19.95px;
            font-weight: 600;
            color: rgba(63, 114, 155, 0.62);
            margin-bottom: 60px;
            /* stylelint-disable */
            font-family: 'Gilroy-Bold' !important;
            /* stylelint-enable */
          }
          button {
            background-color: rgba(63, 114, 155, 0.71);
            font-size: 20px;
            color: #fff;
            font-weight: 900;
            border: none;
            border-radius: 18px;
            width: 180px;
            height: 55px;
            text-align: center;
            box-shadow: 0 0 15px 3px rgba(63, 114, 155, 0.71);
            outline: none;
            /* stylelint-disable */
            font-family: 'Gilroy-Medium' !important;
            /* stylelint-enable */
          }
        }
      }
    }
  }
}
.homepageSection {
  height: 100%;
  min-height: 80vh;
  background-size: cover;
  //background-image: url('../../assets/HomePage/bgSection.png');
  background-position: center;
  display: flex;
  align-items: center;
  /* stylelint-disable */
  font-family: 'Gilroy-Medium' !important;
  /* stylelint-enable */
  .homepageSectionContainer {
    display: grid;
    align-self: normal;
    padding: 0 8%;
    .nameofPlan {
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 60px;
      background-color: rgba(137, 255, 139, 0.11);
      height: 150px;
      .tutorialVid {
        text-decoration: none;
        color: rgb(87, 157, 88);
      }
    }
    .sectionpart {
      text-align: center;
      padding: 0 40px;
      img {
        padding: 20px;
        width: 200px;
        height: 200px;
      }
      .sectionpartTitle {
        color: rgba(0, 53, 84, 0.75);
        font-size: 30px;
        margin-bottom: 10px;
        margin-top: 10px;
      }
      .sectionpartDescr {
        color: rgba(0, 53, 84, 0.61);
        font-size: 16px;
      }
    }
  }
}
.homepageSecDescr {
  background-position: center;
  background-size: cover;
  height: 100%;
  min-height: 70vh;
  display: flex;
  align-items: center;
  .homepageSectionDescr {
    padding: 80px 8% 0 8%;
    display: flex;
    align-items: center;
    height: 100%;
    .homepageSectionDescrColVideo {
      .youtube {
        width: 100% !important;
        iframe {
          width: 100% !important;
          min-height: 400px;
          height: 100% !important;
          border-radius: 30px;
          box-shadow: 0 0 20px 10px rgba(0, 0, 0, 0.26);
        }
      }
    }
    .homepageSectionDescrColDet {
      display: grid;
      justify-content: center;
      align-items: center;
      .homepageSectionDescrColDeth1 {
        margin-bottom: 30px;
        font-size: 30px;
        color: #4d6c72;
        font-family: 'Gilroy-Bold' !important;
        text-align: center;
      }
      .homepageSectionDescrColDetp {
        margin-bottom: 40px;
        padding: 0 40px;
        font-size: 16px;
        color: #5f868d;
        font-family: 'Gilroy-Medium' !important;
        text-align: justify;
      }
      .homepageSectionDescrColDetbutton {
        text-align: center;
        margin: 0 auto;
        font-size: 17px;
        /* stylelint-disable */
        font-family: 'Gilroy-Regular' !important;
        /* stylelint-enable */
        border: none;
        background-color: #c7bba5;
        color: white;
        height: 40px;
        width: 120px;
        border-radius: 50px;
        display: flex;
        align-items: center;
        justify-content: center;
      }
    }
  }
}
.topplusfooter {
  min-height: 50vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: radial-gradient(
    circle,
    rgba(38, 255, 0, 0.21) 0%,
    rgba(213, 213, 213, 0) 25%
  );
  .topplusfootercontainer {
    padding: 0 8%;
    .topplusfooterrow {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 100%;
      .topplusfootercol {
        /* stylelint-disable */
        font-family: 'Gilroy-Medium' !important;
        /* stylelint-enable */
        text-align: center;
        display: grid;
        justify-content: center;
        justify-items: center;
        .topplusfootercolimg {
          height: 100px;
          width: 100px;
          margin-bottom: 10px;
        }
        .topplusfootercolspan {
          color: rgba(37, 42, 55, 0.63);
          font-size: 14px;
          margin-bottom: 10px;
        }
        .topplusfootercolp {
          color: rgba(37, 42, 55, 0.81);
          font-size: 19px;
        }
      }
    }
  }
}
.mainfooter {
  background-image: url('../../assets/HomePage/bgfooter.png');
  background-size: cover;
  min-height: 40vh;
  background-position: center;
  height: 100%;
  display: flex;
  align-items: flex-end;
  padding-bottom: 20px;
  .copyrightcol {
    text-align: center;
    padding-top: 40px;
    .copyright {
      color: rgba(14, 12, 12, 0.98);
      /* stylelint-disable */
      font-family: 'Gilroy-Light' !important;
      /* stylelint-enable */
    }
  }
  .mainfootercollogo {
    display: flex;
    align-items: center;
    justify-content: flex-end;
    .mainfooterlogo {
      width: 150px;
      height: 150px;
    }
  }
  .mainfootercontainer {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 0 8%;
    .mainfooterrow {
      .mainfootercollinks {
        .footerlinks {
          display: grid;
          .footerlink {
            margin: 10px 0;
            text-decoration: none;
            font-size: 16px;
            /* stylelint-disable */
            font-family: 'Gilroy-Medium' !important;
            /* stylelint-enable */
            color: rgba(62, 29, 6, 0.58);
          }
          .footerheadlink {
            margin: 0 0 10px 0;
            font-size: 16px !important;
            /* stylelint-disable */
            font-family: 'Gilroy-Bold' !important;
            /* stylelint-enable */
            color: rgba(60, 28, 5, 0.78);
          }
        }
      }
    }
  }
}
</style>
