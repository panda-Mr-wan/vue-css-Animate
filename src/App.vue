<template>
  <div>
    <h3>使用component组件实现组件的动态切换</h3>
    <!-- 如果把切换出去的组件保留在内存中，可以保留它的状态或避免重新渲染。为此可以添加一个 keep-alive 指令参数： -->
    <keep-alive>
    <component :is="com"></component>
    </keep-alive>
    <button @click="change">点击切换组件</button>
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
        com:"Child"
      }
    },
    methods:{
      change(){
        this.com=this.com=="Child2"?"Child":"Child2"
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>