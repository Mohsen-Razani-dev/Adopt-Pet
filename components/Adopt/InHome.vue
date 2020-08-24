<template>
  <div class="inHome">
    <el-main class="inHomeContainer">
      <el-row class="inHomeRow">
        <el-divider></el-divider>
        <el-col :md="24" v-for="item in items" class="inHomeCol">
          <div class="inHomeItem">
            <img :src="item.img" alt="" />
            <span class="inHomeItemName">{{ item.name }}</span>
            <span class="inHomeItemDescr">{{ item.descr }}</span>
            <nuxt-link class="inHomeItemLink" :to="'/Adopt/inHome/' + item.link"
              >Pick This</nuxt-link
            >
          </div>
          <hr />
        </el-col>
      </el-row>
    </el-main>
    <div>
      <p style="margin: 0 0 70px 0">
        <i
          style="padding: 0 10px; font-size: 20px; color: #eacc00;"
          class="el-icon-warning"
        ></i>
        tips : It is a long established fact that a reader will be distracted by
        the readable content of a page when looking at its layout.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'inHome',
  data() {
    return {
      mountedComponent: true,
      items: [
        {
          id: 1,
          name: 'DOG',
          link: 'Dog',
          img: require('../../assets/Adopt/inHome/dog.jpg'),
          descr:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut faucibus leo et enim vulputate, ut mattis tellus venenatis.',
        },
        {
          id: 2,
          name: 'CAT',
          link: 'Cat',
          img: require('../../assets/Adopt/inHome/cat.jpg'),
          descr:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut faucibus leo et enim vulputate, ut mattis tellus venenatis.',
        },
        {
          id: 3,
          name: 'SNAKE',
          link: 'Snake',
          img: require('../../assets/Adopt/inHome/snake.jpg'),
          descr:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut faucibus leo et enim vulputate, ut mattis tellus venenatis.',
        },
        {
          id: 4,
          name: 'EAGLE',
          link: 'Eagle',
          img: require('../../assets/Adopt/inHome/eagle.jpg'),
          descr:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut faucibus leo et enim vulputate, ut mattis tellus venenatis.',
        },
        {
          id: 5,
          name: 'OWL',
          link: 'Owl',
          img: require('../../assets/Adopt/inHome/owl.jpg'),
          descr:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut faucibus leo et enim vulputate, ut mattis tellus venenatis.',
        },
        {
          id: 6,
          name: 'KOALA',
          link: 'Koala',
          img: require('../../assets/Adopt/inHome/koala.jpg'),
          descr:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut faucibus leo et enim vulputate, ut mattis tellus venenatis.',
        },
        {
          id: 7,
          name: 'PARROT',
          link: 'Parrot',
          img: require('../../assets/Adopt/inHome/parrots.jpg'),
          descr:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut faucibus leo et enim vulputate, ut mattis tellus venenatis.',
        },
        {
          id: 8,
          name: 'HAMSTER',
          link: 'Hamster',
          img: require('../../assets/Adopt/inHome/hamster.jpg'),
          descr:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut faucibus leo et enim vulputate, ut mattis tellus venenatis.',
        },
      ],
    }
  },
}
</script>
<style lang="scss">
.inHome {
  min-height: 100vh;
  height: 100%;
  padding: 100px 8% 0 8%;
  .inHomeContainer {
    .inHomeRow {
      hr {
        border: 1px solid rgba(167, 167, 167, 0.75);
        margin: 15px 0;
      }
      .inHomeHeader {
        font-family: Gilroy-Bold;
        font-size: 45px;
        color: #5a6e5a;
      }
      .inHomeCol {
        .inHomeItem {
          display: flex;
          align-items: center;
          justify-content: space-between;
          background-color: #ececec;
          border-radius: 50px;
          box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.25);
          font-family: Gilroy-Regular;
          img {
            object-fit: cover;
            height: 110px;
            width: 110px;
            border-radius: 100%;
            box-shadow: 0 0 8px 0 rgba(0, 0, 0, 0.34);
            background-color: white;
          }
          .inHomeItemName {
            font-size: 16px;
            color: #243441;
          }
          .inHomeItemDescr{
            font-size: 14px;
            color: #243441;
          }
          a {
            background-color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 110px;
            width: 110px;
            text-decoration: none;
            color: rgba(108, 108, 108, 0.99);
            border-radius: 100%;
            box-shadow: 0 0 8px 0 rgba(0, 0, 0, 0.34);
          }
        }
      }
    }
  }
}
</style>
