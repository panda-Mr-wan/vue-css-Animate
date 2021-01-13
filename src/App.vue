<template>
  <div>
    <h3>App</h3>
    <hr>
    <Child :num-child="num" :message="message" :data="data" :prop-f="propF" />
  </div>
</template>

<script>
  import Child from "./components/Child";
  export default {
    name:"App",
    components:{ Child },
    data(){
      return {
        num:200,
        message:"我是帅哥",
        data:"我是美女",
        propF:'30'
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>