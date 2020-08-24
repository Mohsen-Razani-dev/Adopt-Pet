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
            <img :src="require('../../assets/Clinic/DDDD.png')" alt="" />
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
          <el-col :md="6" class="appointmentDescrCol">
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
          <el-col :md="10" class="appointmentSubmitCol">
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
          <el-col :md="6" class="ContactDoctorCol">
            <div class="ContactDoctorBox">
              <i class="el-icon-message"></i>
              <h1>Email</h1>
              <div>
                <span>mohsenrazani@gmail.com</span>
                <span>mohsenrazani@gmail.com</span>
              </div>
            </div>
          </el-col>
          <el-col :md="6" class="ContactDoctorCol">
            <div class="ContactDoctorBox">
              <i class="el-icon-message"></i>
              <h1>Email</h1>
              <div>
                <span>mohsenrazani@gmail.com</span>
                <span>mohsenrazani@gmail.com</span>
              </div>
            </div>
          </el-col>
          <el-col :md="6" class="ContactDoctorCol">
            <div class="ContactDoctorBox">
              <i class="el-icon-message"></i>
              <h1>Email</h1>
              <div>
                <span>mohsenrazani@gmail.com</span>
                <span>mohsenrazani@gmail.com</span>
              </div>
            </div>
          </el-col>
          <el-col :md="6" class="ContactDoctorCol">
            <div class="ContactDoctorBox">
              <i class="el-icon-message"></i>
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
        <el-col :md="6" class="footerCol">
          <img src="../../assets/logopet.png" alt="" width="50" height="50" />
          <p>
            Leading the way in Media <br />
            Exellence. Trusted Care
          </p>
        </el-col>
        <el-col :md="6" class="footerCol" style="justify-content: center;">
          <span>Important Links</span>
          <a href="#">Appointment</a>
          <a href="#">Doctors</a>
          <a href="#">Services</a>
          <a href="#">About Us</a>
        </el-col>
        <el-col :md="6" class="footerCol" style="justify-content: center;">
          <span>Contact Us</span>
          <a href="#">Call: (021) - 888 -44345</a>
          <a href="#">Email: MohsenRazani.z@gmail.com</a>
          <a href="#">Address: Iran - Tehran - 4545</a>
        </el-col>
        <el-col :md="6" class="footerCol" style="justify-content: center;">
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
import Appointment from '~/components/Clinic/Appointment'
export default {
  name: 'Clinic',
  components: { Appointment },
  data: () => ({
    specialties: [
      {
        id: 1,
        img: require('../../assets/Clinic/clinicItems/png/003-checkup.png'),
        name: 'Checkup',
        specialtiesitems: ['embarrassing', 'Clinic', 'ultrasound'],
      },
      {
        id: 2,
        img: require('../../assets/Clinic/clinicItems/png/048-ultrasound.png'),
        name: 'Radiology',
      },
      {
        id: 3,
        img: require('../../assets/Clinic/clinicItems/png/029-blood-bag.png'),
        name: 'Blood Test',
      },
      {
        id: 4,
        img: require('../../assets/Clinic/clinicItems/png/026-health-report.png'),
        name: 'Monthly Report',
      },
      {
        id: 5,
        img: require('../../assets/Clinic/clinicItems/png/030-litter-box.png'),
        name: 'Stool Test',
      },
      {
        id: 6,
        img: require('../../assets/Clinic/clinicItems/png/012-declawing.png'),
        name: 'Declawing',
      },
      {
        id: 7,
        img: require('../../assets/Clinic/clinicItems/png/043-pet-food.png'),
        name: 'Diet',
      },
      {
        id: 8,
        img: require('../../assets/Clinic/clinicItems/png/057-insecticide.png'),
        name: 'Parasitization',
      },
    ],
    doctors: [
      {
        id: 1,
        name: 'Mohsen Razani',
        img: require('../../assets/Clinic/Doctors/1.png'),
      },
      {
        id: 2,
        name: 'Hossein Razani',
        img: require('../../assets/Clinic/Doctors/6.png'),
      },
      {
        id: 3,
        name: 'Sajjad Kazemi',
        img: require('../../assets/Clinic/Doctors/5.png'),
      },
      {
        id: 4,
        name: 'Hassan Kazemi',
        img: require('../../assets/Clinic/Doctors/2.png'),
      },
      {
        id: 5,
        name: 'Mohsen Razani',
        img: require('../../assets/Clinic/Doctors/3.png'),
      },
      {
        id: 6,
        name: 'Mohsen Razani',
        img: require('../../assets/Clinic/Doctors/4.png'),
      },
    ],
  }),
}
</script>

<style scoped lang="scss">
.clinic {
  .headerClinic {
    background-image: url('../../assets/Clinic/hederbg.png');
    background-size: cover;
    background-position: center;
    width: 100%;
    min-height: 80vh;
    display: flex;
    align-items: center;
    justify-content: center;
    .containerClinic {
      padding: 0 8%;
      .containerClinicHeaderDescr {
        .containerClinicHeaderDescrbox {
          span {
            font-size: 28px;
            color: #6d8ba7;
          }
          h1 {
            font-size: 60px;
            color: #304f6e;
          }
          button {
            font-family: Gilroy-Medium;
            padding: 15px 25px;
            background-color: #46b6f6;
            font-size: 15px;
            color: white;
            border: none;
            border-radius: 4px;
          }
        }
      }
    }
  }
  .sectionClinic {
    margin-top: 40px;
    .sectionClinicRow {
      justify-content: center;
      align-items: center;
      display: flex;
      overflow: hidden;
      .sectionClinicCol {
        text-align: center;
        img {
          width: 100%;
          margin-bottom: -20px;
          margin-top: 70px;
        }
        .sectionClinicP {
          font-size: 18px;
          font-family: Gilroy-Regular;
          margin-bottom: 8px;
          color: #6d8ba7;
        }
        .sectionClinicH {
          color: #304f6e;
          font-size: 36px;
          font-family: Gilroy-Medium;
          margin-bottom: 16px;
        }
        .sectionClinicSpan {
          color: #355173;
          font-size: 15px;
          font-family: Gilroy-Regular;
          margin-bottom: 10px;
        }
        .sectionClinicA {
          text-decoration: none;
          color: #46b6f6;
        }
      }
    }
  }
  .clinicSpecialties {
    padding: 0 4%;
    margin-bottom: 40px;
    .clinicSpecialtiesheader {
      text-align: center;
      .clinicSpecialtiesheaderP {
        color: #6d8ba7;
      }
      .clinicSpecialtiesheaderH {
        color: #304f6e;
      }
    }
    .clinicSpecialtiesRow {
      display: flex;
      justify-content: center;
      .clinicSpecialtiesCol {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        align-items: center;
        margin-top: 50px;
        .clinicSpecialtiesboxCol {
          border-collapse: collapse;
          padding: 7px;
          .clinicSpecialtiesbox {
            border-radius: 4px;
            box-shadow: 0 0 7px 1px rgba(0, 0, 0, 0.53);
            background-color: white;
            transition: 200ms all ease-out;
            position: relative;
            display: grid;
            justify-content: center;
            align-items: center;
            text-align: center;
            .clinicSpecialtiesImg {
              width: 100%;
              padding: 50px 50px 0 50px;
            }
            .clinicSpecialtiesDesc {
              text-align: center;
              position: absolute;
              width: 100%;
              left: 50%;
              top: 50%;
              margin: 0 auto;
              transform: translate(-50%, -50%);
              background-color: rgba(70, 182, 246, 0.85);
              color: white;
              font-family: Gilroy-Bold;
              font-size: 25px;
              height: 100%;
              display: none;
              align-items: center;
              justify-content: center;
            }
            .clinicSpecialtiesName {
              padding: 20px 0 50px 0;
              color: #355173;
            }
            &:hover {
              transform: scale(1.05);
              transition: 200ms all ease-out;
              box-shadow: 0 0 30px 10px rgba(70, 182, 246, 0.33);
              border: none;
              .clinicSpecialtiesDesc {
                display: flex;
                .clinicSpecialtiesDescUl {
                  width: 100%;
                  text-align: left;
                  padding-left: 30px;
                  height: 100%;
                  padding-top: 40px;
                  .clinicSpecialtiesDescHeader {
                    font-size: 17px;
                    list-style: none;
                    text-align: left;
                    width: 100%;
                    margin-bottom: 10px;
                  }
                  .clinicSpecialtiesDescLi {
                    font-size: 15px;
                  }
                }
              }
            }
          }
        }
      }
    }
  }
  .appointment {
    background-image: url('../../assets/Clinic/hush-naidoo-yo01Z-9HQAw-unsplash.jpg');
    background-size: cover;
    background-position: center;
    min-height: 70vh;
    height: 100%;
    position: relative;
    .appointmentMain {
      overflow: hidden;
      position: absolute;
      height: 100%;
      background-color: rgba(73, 186, 244, 0.89);
      width: 100%;
      background-size: cover;
      .appointmentRow {
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100%;
        .appointmentDescrCol{
          .appointmentDescr{
            .appointmentH{
              color: #FFF;
              font-family: Gilroy-Regular;
              margin-bottom: 40px;
              font-size: 33px;
            }
            .appointmentDescrP{
              color: #FFF;
              font-family: Gilroy-Regular;
            }
          }
        }
        .appointmentSubmitCol {
          .submitForm {
            padding: 80px;
          }
        }
      }
    }
  }
  .doctors {
    /*background-color: white;*/
    min-height: 90vh;
    .doctorsMain {
      height: 100%;
      .doctorsHeaderDescr {
        text-align: center;
        width: 100%;
        padding: 50px 0;
        span {
          font-size: 20px;
          color: #6d8ba7;
        }
        h1 {
          font-size: 40px;
          color: #304f6e;
        }
      }
      .doctorsRow {
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        .doctorsCol {
          .doctorCarousel {
            min-height: 80vh;
            height: 100%;
            .doctorCarouselItem {
              height: auto !important;
              padding: 20px;
              .doctorCarouselCard {
                box-shadow: 0 0 20px 0 rgba(50, 49, 49, 0.75);
                background-color: white;
                text-align: center;
                padding: 0;
                height: auto;
                width: 350px;
                height: 100%;
                margin: 0 auto;
                .doctorCarouselDescribtion {
                  background-color: #edf4fa;
                  z-index: 10;
                  .doctorCarouselName {
                    padding-top: 30px;
                    padding-bottom: 20px;
                  }
                  .doctorCarouselAbility {
                    padding-bottom: 30px;
                  }
                  .drmedia {
                    padding-bottom: 30px;
                    display: flex;
                    justify-content: center;
                    i {
                      color: white;
                      padding: 8px;
                      margin-right: 7px;
                      background-color: rgb(69, 183, 241);
                    }
                  }
                  .ViewProfile {
                    width: 100%;
                    background-color: rgba(69, 183, 241, 0.94);
                    color: white;
                    height: 60px;
                    font-size: 24px;
                    cursor: pointer;
                    border: none;
                    outline: none;
                  }
                }
                .doctorCarouselImg {
                  margin-bottom: -3px;
                  padding: 30px 30px 0 30px;
                  max-height: 300px;
                  width: 100%;
                  object-fit: contain;
                  z-index: 1;
                }
              }
            }
          }
        }
      }
    }
  }
  .ContactDoctor {
    padding: 0 8%;
    .ContactDoctorsMain {
      .ContactDoctorRow {
        .ContactDoctorCol {
          padding: 30px;
          .ContactDoctorBox {
            padding: 30px;
            background-color: #ececec;
            height: 240px;
            width: 240px;
            display: grid;
            align-items: center;
            align-content: space-evenly;
            cursor: pointer;
            i {
              font-size: 40px;
              color: rgb(84, 192, 246);
            }
            h1 {
              font-size: 22px;
              font-family: Gilroy-Medium;
              color: #304f6e;
            }
            span {
              font-family: Gilroy-Medium;
              font-size: 14px;
              color: #6d8ba7;
            }
            &:hover {
              background-color: rgb(84, 192, 246);
              i,
              h1,
              span {
                color: rgba(255, 255, 255, 0.92);
              }
            }
          }
        }
      }
      .ContactDoctorsHeaderDescr {
        text-align: center;
        width: 100%;
        padding: 50px 0;
        span {
          font-size: 20px;
          color: #6d8ba7;
        }
        h1 {
          font-size: 40px;
          color: #304f6e;
        }
      }
    }
  }
  .footer {
    padding: 70px 8% 40px 8%;
    background-color: #304f6e;
    .Copyright {
      color: rgba(255, 255, 255, 0.91);
      font-size: 12px;
    }
    .footerCol {
      display: grid;
      align-items: flex-start;
      padding: 0 20px;
      p {
        margin-top: 15px;
        font-size: 17px;
        color: rgba(255, 255, 255, 0.81);
      }
      span {
        font-size: 19px;
        color: rgba(255, 255, 255, 0.89);
        margin-bottom: 15px;
      }
      a {
        margin-top: 12px;
        text-decoration: none;
        font-size: 15px;
        color: rgba(255, 255, 255, 0.75);
      }
    }
  }
  .FindDoctor {
    width: 100%;
    display: flex;
    justify-content: center;
    margin-top: -50px;
    #Application {
      background-color: #46b6f6;
    }
    #Find {
      background-color: #aedc46;
    }
    #Charge {
      background-color: #46b6f6;
    }
    button {
      cursor: pointer;
      margin: 0 40px;
      color: white;
      height: 90px;
      width: 290px;
      font-size: 27px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 15px;
      border: none;
      i {
        font-size: 33px;
      }
    }
  }
}
.el-carousel__container {
  position: relative;
  height:auto ;
}
</style>
