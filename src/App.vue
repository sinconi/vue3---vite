<script>
  import messageItem from './components/messageItem.vue'
  import messageItem2 from './components/messageItem2.vue'


  export default {
    components: {
      messageItem,
      messageItem2
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
        ]
      }
    },
  }
</script>

<template>
  <messageItem sender="nini" msg="今天吃麥當勞" time="12:00"></messageItem>
  <hr>
  <!-- 動態獲取 -->
  <messageItem2 v-for="msgList in message" :key="msgList.id" :sender="msgList.sender" :msg="msgList.msg"
    :time="msgList.time"></messageItem2>

  <hr>
  <messageItem2 v-for="msgList in message" :key="msgList.id" v-bind="msgList"></messageItem2>
</template>

<style scoped>

</style>