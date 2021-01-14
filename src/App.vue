<template>
  <div>
    <h3>App组件</h3>
    <p>祖先组件的属性值message:{{ message }}</p>
    <p>祖先组件的属性值name:{{ obj.name | checkName }}</p>
    <hr>
    <Child />
    <hr>
    <Child2 />
  </div>
</template>

<script>
  import Vue from "vue";
  // 组册全局filter
  Vue.filter("checkName",name => {
    if(name=="jarry"){
      return "Join Hanks"
    }
    return name;
  })
  import Child from "./components/Child";
  import Child2 from "./components/Child2";
  export default {
    name:"App",
    components:{ Child, Child2 },
    data(){
      return {
        message:"我是大帅哥",
        changeMsg:this.changeMessage,
        obj:{name:"tom"}
      }
    },
    methods:{
      changeMessage(msg){
        this.message=msg
      }
    },
    provide(){
      return {
        msg:this.message,
        change:this.changeMsg,
        obj:this.obj
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>