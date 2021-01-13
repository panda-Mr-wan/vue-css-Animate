<template>
  <div>
    <h3>App组件</h3>
    <Child />
    <hr>
    <Child2 />
  </div>
</template>

<script>
  import Child from "./components/Child";
  import Child2 from "./components/Child2";
  export default {
    name:"App",
    components:{ Child,Child2 },
  }
</script>

<style lang="scss" scoped>

</style>