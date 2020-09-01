<template>
  <div class="clinic">
    <div class="headerClinic">
      <el-main class="containerClinic">
        <el-row class="containerClinicHeaderDescr">
          <el-col :md="24">
            <div class="containerClinicHeaderDescrbox">
              <span>Caring for Life</span>
              <h1>
                Leading the Way <br />
                in Medical Exellence
              </h1>
              <button>
                Our Services <i class="el-icon-arrow-right el-icon-right"></i>
              </button>
            </div>
          </el-col>
        </el-row>
      </el-main>
    </div>
    <div class="FindDoctor">
      <button id="Application">
        Get Application <i class="el-icon-mobile"></i>
      </button>
      <button id="Find">Find a Doctor <i class="el-icon-service"></i></button>
      <button id="Charge">
        Asking Questions <i class="el-icon-chat-line-square"></i>
      </button>
    </div>
    <div class="sectionClinic">
      <el-main style="padding-bottom: 0 !important;">
        <el-row class="sectionClinicRow">
          <el-col :md="12" class="sectionClinicCol">
            <P class="sectionClinicP">Welcome to clinic</P>
            <h1 class="sectionClinicH">A Great Place to Receive Care</h1>
            <p class="sectionClinicSpan">
              There are many variations of passages of Lorem Ipsum available,
              but the majority have suffered alteration in some form, by
              injected humour, or randomised words which don't look even
              slightly believable. If you are going to use a passage of Lorem
              Ipsum, you need to be sure there isn't anything embarrassing
              hidden in the middle of text.
            </p>
            <a class="sectionClinicA" href="#"
              >Learn More <i class="el-icon-arrow-right"></i
            ></a>
            <img :src="require('../../assets/Images/Clinic/DDDD.png')" alt="" />
          </el-col>
        </el-row>
      </el-main>
    </div>
    <div class="clinicSpecialties">
      <el-main style="background-color: #f6f6f6; border-radius: 10px;">
        <div class="clinicSpecialtiesheader">
          <p class="clinicSpecialtiesheaderP">Alwayse Caring</p>
          <h1 class="clinicSpecialtiesheaderH">Our specialties</h1>
        </div>
        <el-row class="clinicSpecialtiesRow">
          <el-col :md="14" class="clinicSpecialtiesCol">
            <el-row>
              <el-col
                :md="6"
                :sm="8"
                class="clinicSpecialtiesboxCol"
                v-for="item in specialties"
                v-bind:key="specialties.id"
              >
                <div class="clinicSpecialtiesbox">
                  <img class="clinicSpecialtiesImg" :src="item.img" alt="..." />
                  <p class="clinicSpecialtiesName">{{ item.name }}</p>
                  <span class="clinicSpecialtiesDesc">
                    <ul class="clinicSpecialtiesDescUl">
                      <li class="clinicSpecialtiesDescHeader">Abilities</li>
                      <li
                        v-for="SpecItem in item.specialtiesitems"
                        class="clinicSpecialtiesDescLi"
                      >
                        {{ SpecItem }}
                      </li>
                    </ul>
                  </span>
                </div>
              </el-col>
            </el-row>
          </el-col>
        </el-row>
      </el-main>
    </div>
    <div class="appointment">
      <el-main class="appointmentMain">
        <el-row class="appointmentRow">
          <el-col :md="6" :sm="20" class="appointmentDescrCol">
            <div class="appointmentDescr">
              <h1 class="appointmentH">Make an Appointment</h1>
              <p class="appointmentDescrP">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever since the 1500s, when an unknown printer took a galley
                of type and scrambled it to make a type specimen book.
              </p>
            </div>
          </el-col>
          <el-col :md="10" :sm="20" class="appointmentSubmitCol">
            <div class="submitForm">
              <Appointment />
            </div>
          </el-col>
        </el-row>
      </el-main>
    </div>
    <div class="doctors">
      <el-main class="doctorsMain">
        <div class="doctorsHeaderDescr">
          <span>Trusted Care</span>
          <h1>Our Doctors</h1>
        </div>
        <el-row class="doctorsRow">
          <el-col :md="18" class="doctorsCol">
            <el-carousel
              class="doctorCarousel"
              :interval="4000"
              type="card"
              arrow="never"
              indicator-position="none"
            >
              <el-carousel-item
                class="doctorCarouselItem"
                v-for="item in doctors"
                :key="item.id"
              >
                <div class="doctorCarouselCard">
                  <img class="doctorCarouselImg" :src="item.img" alt="" />
                  <div class="doctorCarouselDescribtion">
                    <h3 class="doctorCarouselName">{{ item.name }}</h3>
                    <p class="doctorCarouselAbility">Neurology</p>
                    <div class="drmedia">
                      <i class="el-icon-document"></i>
                      <i class="el-icon-document"></i>
                      <i class="el-icon-document"></i>
                      <i class="el-icon-document"></i>
                    </div>
                    <button class="ViewProfile">
                      View Profile
                    </button>
                  </div>
                </div>
              </el-carousel-item>
            </el-carousel>
          </el-col>
        </el-row>
      </el-main>
    </div>
    <div class="ContactDoctor">
      <el-main class="ContactDoctorsMain">
        <div class="ContactDoctorsHeaderDescr">
          <span>Get in touch</span>
          <h1>Contact</h1>
        </div>
        <el-row class="ContactDoctorRow">
          <el-col :md="6" :sm="12" class="ContactDoctorCol">
            <div class="ContactDoctorBox">
              <i class="el-icon-message"></i>
              <h1>Email</h1>
              <div>
                <span>mohsenrazani@gmail.com</span>
                <span>mohsenrazani@gmail.com</span>
              </div>
            </div>
          </el-col>
          <el-col :md="6" :sm="12" class="ContactDoctorCol">
            <div class="ContactDoctorBox">
              <i class="el-icon-phone"></i>
              <h1>Email</h1>
              <div>
                <span>mohsenrazani@gmail.com</span>
                <span>mohsenrazani@gmail.com</span>
              </div>
            </div>
          </el-col>
          <el-col :md="6" :sm="12" class="ContactDoctorCol">
            <div class="ContactDoctorBox">
              <i class="el-icon-user-solid"></i>
              <h1>Email</h1>
              <div>
                <span>mohsenrazani@gmail.com</span>
                <span>mohsenrazani@gmail.com</span>
              </div>
            </div>
          </el-col>
          <el-col :md="6" :sm="12" class="ContactDoctorCol">
            <div class="ContactDoctorBox">
              <i class="el-icon-office-building"></i>
              <h1>Email</h1>
              <div>
                <span>mohsenrazani@gmail.com</span>
                <span>mohsenrazani@gmail.com</span>
              </div>
            </div>
          </el-col>
        </el-row>
      </el-main>
    </div>
    <footer class="footer">
      <el-row>
        <el-col :md="6" :sm="18" class="footerCol" id="ClinicfooterColLogo">
          <img
            src="../../assets/Images/logopet.png"
            alt=""
            width="50"
            height="50"
          />
          <p>
            Leading the way in Media
            Exellence. Trusted Care
          </p>
        </el-col>
        <el-col :md="6" :sm="8" class="footerCol" style="justify-content: center;">
          <span>Important Links</span>
          <a href="#">Appointment</a>
          <a href="#">Doctors</a>
          <a href="#">Services</a>
          <a href="#">About Us</a>
        </el-col>
        <el-col :md="6" :sm="8" class="footerCol" style="justify-content: center;">
          <span>Contact Us</span>
          <a href="#">Call: (021) - 888 -44345</a>
          <a href="#">Email: MohsenRazani.z@gmail.com</a>
          <a href="#">Address: Iran - Tehran - 4545</a>
        </el-col>
        <el-col :md="6" :sm="8" class="footerCol" style="justify-content: center;">
          <span>Newsletter</span>
          <el-input placeholder="Pick a date" suffix-icon="el-icon-date">
          </el-input>
        </el-col>
        <el-col :md="24">
          <el-divider></el-divider>
          <span class="Copyright"
            >Copyright © 2020 Mohsen Razani. All right Reserved</span
          >
        </el-col>
      </el-row>
    </footer>
  </div>
</template>

<script>
import '../../assets/Styles/Clinic.scss'
import Appointment from '~/components/Clinic/Appointment'
export default {
  name: 'Clinic',
  components: { Appointment },
  data: () => ({
    specialties: [
      {
        id: 1,
        img: require('../../assets/Images/Clinic/clinicItems/png/003-checkup.png'),
        name: 'Checkup',
        specialtiesitems: ['embarrassing', 'Clinic', 'ultrasound'],
      },
      {
        id: 2,
        img: require('../../assets/Images/Clinic/clinicItems/png/048-ultrasound.png'),
        name: 'Radiology',
      },
      {
        id: 3,
        img: require('../../assets/Images/Clinic/clinicItems/png/029-blood-bag.png'),
        name: 'Blood Test',
      },
      {
        id: 4,
        img: require('../../assets/Images/Clinic/clinicItems/png/026-health-report.png'),
        name: 'Monthly Report',
      },
      {
        id: 5,
        img: require('../../assets/Images/Clinic/clinicItems/png/030-litter-box.png'),
        name: 'Stool Test',
      },
      {
        id: 6,
        img: require('../../assets/Images/Clinic/clinicItems/png/012-declawing.png'),
        name: 'Declawing',
      },
      {
        id: 7,
        img: require('../../assets/Images/Clinic/clinicItems/png/043-pet-food.png'),
        name: 'Diet',
      },
      {
        id: 8,
        img: require('../../assets/Images/Clinic/clinicItems/png/057-insecticide.png'),
        name: 'Parasitization',
      },
    ],
    doctors: [
      {
        id: 1,
        name: 'Mohsen Razani',
        img: require('../../assets/Images/Clinic/Doctors/1.png'),
      },
      {
        id: 2,
        name: 'Hossein Razani',
        img: require('../../assets/Images/Clinic/Doctors/6.png'),
      },
      {
        id: 3,
        name: 'Sajjad Kazemi',
        img: require('../../assets/Images/Clinic/Doctors/5.png'),
      },
      {
        id: 4,
        name: 'Hassan Kazemi',
        img: require('../../assets/Images/Clinic/Doctors/2.png'),
      },
      {
        id: 5,
        name: 'Mohsen Razani',
        img: require('../../assets/Images/Clinic/Doctors/3.png'),
      },
      {
        id: 6,
        name: 'Mohsen Razani',
        img: require('../../assets/Images/Clinic/Doctors/4.png'),
      },
    ],
  }),
}
</script>
