<script>
  import messageItem from './components/messageItem.vue'
  import messageItem2 from './components/messageItem2.vue'
  import blogPostItem from './components/blogPostItem.vue'
  import card from './components/card.vue'
  import blogPostItem2 from './components/blogPostItem2.vue'




  export default {
    components: {
      messageItem,
      messageItem2,
      blogPostItem,
      card,
      blogPostItem2
    },
    data() {
      return {
        message: [
          {
            id: 1,
            sender: 'nini1',
            msg: '今天吃麥當勞',
            time: '12:00'
          },
          {
            id: 2,
            sender: 'nini2',
            msg: '今天吃麥當勞',
            time: '12:00'
          },
          {
            id: 3,
            sender: 'nini3',
            msg: '今天吃麥當勞',
            time: '12:00'
          }
        ],
        posts: [
          {
            id: 1,
            title: 'post1',
            link: 'https://www.google.com/'
          },
          {
            id: 2,
            title: 'post2',
            link: 'https://www.google.com/'
          },
          {
            id: 3,
            title: 'post3',
            link: 'https://www.google.com/'
          },
        ]
      }
    },
    methods: {
      handleDeletePost(id) {
        this.posts = this.posts.filter((p) => p.id !== id);
        console.log(this.post.id)
      }
    }
  }
</script>

<template>
  <!-- <messageItem sender="nini" msg="今天吃麥當勞" time="12:00"></messageItem> -->
  <!-- <hr> -->
  <!-- 動態獲取 -->
  <!-- <messageItem2 v-for="msgList in message" :key="msgList.id" :sender="msgList.sender" :msg="msgList.msg"
    :time="msgList.time"></messageItem2> -->

  <!-- <hr> -->
  <!-- <messageItem2 v-for="msgList in message" :key="msgList.id" v-bind="msgList"></messageItem2> -->

  <div>
    <!-- 在組件上設置class相當於直接對此元件最外層添增class屬性 -->
    <!-- <blogPostItem v-for="post in posts" :key="post.id" v-bind="post" class="blogLink"></blogPostItem> -->

    <!-- slot -->
    <!-- <card title="卡片">
      <p>這是卡片內容</p>
    </card>
    <card #title>
      <h2>這是卡卡</h2>
    </card>
    <card v-slot:content>
      <p>這是卡片內容2</p>
      <p>這是卡片內容2</p>
      <p>這是卡片內容2</p>
    </card> -->


    <!-- emit -->
    <blogPostItem2 v-for="post in posts" :key="post.id" v-bind="post" @deletePost="handleDeletePost">
    </blogPostItem2>
  </div>

</template>

<style scoped>

</style>