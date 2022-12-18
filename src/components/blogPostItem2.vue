<template>
  <div>
    <a :href="link">{{title}}</a>
    <button @click="$emit('deletePost', id)">刪除</button>
  </div>
</template>
<script>
  export default {
    props: ['id', 'link', 'title'],
    emits: ["deletePost"]
  }
</script>
<style lang="">

</style>