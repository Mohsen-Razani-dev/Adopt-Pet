<template>
  <div>
    <div class="blog">
      <div class="blogCont">
        <el-main class="blogMAin">
          <el-row>
            <el-col :md="24">
              <div class="blogHeadBox">
                <p>
                  Stories About Life,<br />
                  Tech & Insurance
                </p>
                <span>
                  Subscribe to our exclusive mailing list and get the freshest
                  stories <br />
                  from the Lemonade team
                </span>
                <div class="mailbox">
                  <input placeholder="EMAIL ADDRESS" type="text" />
                  <button>SUBSCRIBE</button>
                </div>
              </div>
            </el-col>
          </el-row>
        </el-main>
      </div>
    </div>

    <div class="blogPosts">
      <el-main>
        <el-row style="overflow: auto;">
          <el-col :md="8" :sm="12" class="postCol" v-for="item in posts">
            <div class="post">
              <img :src="item.img" alt="..." />
              <h1>
                {{ item.title }}
              </h1>
              <span class="writer">Team Lemonade</span>
              <p>
                {{ item.description }}
              </p>
              <el-tag class="tag" type="info">{{ item.tag }}</el-tag>
            </div>
          </el-col>
        </el-row>
      </el-main>
    </div>
  </div>
</template>

<script>
import '../../assets/Styles/Blog.scss'
export default {
  name: 'Blog',
  data: () => ({
    posts: [
      {
        id: 1,
        img: require('../../assets/Images/blog/posts/post.jpg'),
        title:
          '7 Things To Consider When Picking the Right Dog for Your Lifestyle',
        description:
          'Adopting a furry friend? You’ll want to think about your apartment, the weather, finances, and more. But with a little research you’ll find your new BFF.',
        tag: '#Pet',
      },
      {
        id: 2,
        img: require('../../assets/Images/blog/posts/post.jpg'),
        title:
          '7 Things To Consider When Picking the Right Dog for Your Lifestyle',
        description:
          'Adopting a furry friend? You’ll want to think about your apartment, the weather, finances, and more. But with a little research you’ll find your new BFF.',
        tag: '#Pet',
      },
      {
        id: 3,
        img: require('../../assets/Images/blog/posts/post.jpg'),
        title:
          '7 Things To Consider When Picking the Right Dog for Your Lifestyle',
        description:
          'Adopting a furry friend? You’ll want to think about your apartment, the weather, finances, and more. But with a little research you’ll find your new BFF.',
        tag: '#Pet',
      },
      {
        id: 4,
        img: require('../../assets/Images/blog/posts/post.jpg'),
        title:
          '7 Things To Consider When Picking the Right Dog for Your Lifestyle',
        description:
          'Adopting a furry friend? You’ll want to think about your apartment, the weather, finances, and more. But with a little research you’ll find your new BFF.',
        tag: '#Pet',
      },
    ],
  }),
}
</script>
