<template>
  <div class="instreet">
    <el-main class="instreetContainer">
      <el-row class="instreetRow">
        <el-divider></el-divider>
        <el-col :md="24" v-for="item in items" class="instreetCol">
          <div class="instreetItem">
            <img :src="item.img" alt="" />
            <span class="instreetItemName">{{ item.name }}</span>
            <span class="instreetItemDescr">{{ item.descr }}</span>
            <nuxt-link
              class="instreetItemLink"
              :to="'/Adopt/inStreet/' + item.link"
              >Pick This</nuxt-link
            >
          </div>
          <hr>
        </el-col>
      </el-row>
    </el-main>
    <div>
      <p style="padding: 0 8%;">
        <i style="padding: 0 10px; font-size: 20px; color: #eacc00;" class="el-icon-warning"></i>
        tips : It is a long established fact that a reader will be distracted by
        the readable content of a page when looking at its layout.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'InStreet',
  data() {
    return {
      mountedComponent: true,
      items: [
        {
          id: 1,
          name: 'Food',
          link: 'food',
          img: require('../../assets/Adopt/inStreet/feed.png'),
          descr:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut faucibus leo et enim vulputate, ut mattis tellus venenatis.',
        },
        {
          id: 2,
          name: 'House',
          link: 'house',
          img: require('../../assets/Adopt/inStreet/house1.png'),
          descr:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut faucibus leo et enim vulputate, ut mattis tellus venenatis.',
        },
        {
          id: 3,
          name: 'Treatment',
          link: 'treatment',
          img: require('../../assets/Adopt/inStreet/hospital.png'),
          descr:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut faucibus leo et enim vulputate, ut mattis tellus venenatis.',
        },
        {
          id: 4,
          name: 'Adore',
          link: 'adore',
          img: require('../../assets/Adopt/inStreet/Cuddling.jpg'),
          descr:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut faucibus leo et enim vulputate, ut mattis tellus venenatis.',
        },
      ],
    }
  },
}
</script>

<style scoped lang="scss">
.instreet {
  min-height: 100vh;
  height: 100%;
  padding: 100px 8% 0 8%;
  .instreetContainer {
    .instreetRow {
      hr{
        border: 1px solid rgba(167, 167, 167, 0.75);
        margin: 15px 0;
      }
      .instreetHeader {
        font-family: Gilroy-Bold;
        font-size: 45px;
        color: #5a6e5a;
      }
      .instreetCol {
        .instreetItem {
          display: flex;
          align-items: center;
          justify-content: space-between;
          background-color: #ececec;
          border-radius: 50px;
          font-family: Gilroy-Regular;
          img {
            height: 90px;
            width: 90px;
            padding: 10px;
            border-radius: 100%;
            box-shadow: 0 0 8px 0 rgba(0, 0, 0, 0.34);
            background-color: white;
          }
          .instreeItemName {
            font-size: 16px;
            color: #243441;
          }
          .instreeItemDescr{
            font-size: 14px;
            color: #243441;
          }
          a{
            background-color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 90px;
            width: 90px;
            text-decoration: none;
            color: rgba(108,108,108,0.99);
            border-radius: 100%;
            box-shadow: 0 0 8px 0 rgba(0, 0, 0, 0.34);
          }
        }
      }
    }
  }
}
</style>
