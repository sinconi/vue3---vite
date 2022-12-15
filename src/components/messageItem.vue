<template>
  <div>
    <p>{{sender}}</p>
    <p>{{time}}</p>
    <p>{{msg}}</p>
  </div>


</template>

<script>
  export default {
    props: ["sender", "time", "msg"]
  }


</script>



<style scoped>

</style>