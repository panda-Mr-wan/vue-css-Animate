<template>
  <div>
    <h3>App组件</h3>
    <p>自组件传递过来的属性值：{{message}}</p>
    <Child @myEvent="changeMsg" />
    <hr>
    <Child2 ref="child2" />
  </div>
</template>

<script>
  import Child from "./components/Child";
  import Child2 from "./components/Child2";
  export default {
    name:"App",
    components:{ Child, Child2 },
    data(){
      return {
        message:""
      }
    },
    methods:{
      changeMsg(msg){
        this.message=msg;
      }
    },
    mounted(){
      this.$refs.child2.$on("myEvent",msg => {
        this.message=msg;
      })
    }
  }
</script>

<style lang="scss" scoped>

</style>