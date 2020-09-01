<template>
  <div>
    <div class="homepageheader">
      <el-container class="homepageContainer">
        <el-row class="homepageRow">
          <el-col :xs="24" :md="15" :xl="15" class="homepageColDescr">
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
          <el-col :xs="0" :md="9" :xl="9" class="homepageColSign">
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
              <img
                src="../../assets/Images/HomePage/Vectors/001-plant.png"
                alt=""
              />
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
              <img
                src="../../assets/Images/HomePage/Vectors/002-green.png"
                alt=""
              />
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
              <img
                src="../../assets/Images/HomePage/Vectors/003-modern.png"
                alt=""
              />
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
        <el-row class="homepageSecDescrRow">
          <el-col :sm="20" :md="14" class="homepageSectionDescrColVideo">
            <youtube
              class="youtube"
              :player-vars="{ autoplay: 0 }"
              video-id="tY-6MLpJSqY"
            />
          </el-col>
          <el-col :sm="20" :md="10" class="homepageSectionDescrColDet">
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
              src="../../assets/Images/HomePage/Vectors/004-earth-day.png"
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
            <el-row class="mainfooterrowCols">
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
              src="../../assets/Images/logopet.png"
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
import '../../assets/Styles/Homepage.scss'
import HomepageJoin from '~/components/HomePage/Signupform'
export default {
  name: 'HomePage',
  components: { HomepageJoin },
  data: () => ({}),
}
</script>
