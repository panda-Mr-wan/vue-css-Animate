<template>
  <div>
    <h3>App组件</h3>
    <button @click="show=!show">点击显示或隐藏</button>
    <transition name="fade">
      <p v-if="show">执行动画</p>
    </transition>
    <hr>
    <Child />
    <hr>
    <Child2 />
  </div>
</template>

<script>
  import Child from "./components/Child";
  import Child2 from "./components/Child2";
  export default {
    name:'App',
    components:{ Child, Child2 },
    data(){
      return {
        show:false
      }
    }
  }
</script>

<style lang="css" scoped>
p{
  width:200px;
  height:200px;
  background:#f00;
}
.fade-enter,.fade-leave-to{
  opacity: 0;
  transform: rotate(720deg);
}
.fade-enter-active,.fade-leave-active{
  transition:opacity .3s ease-in 0s,transform .3s ease-in 0s;
}
.fade-enter-to,.fade-leave{
  opacity:1;
}
</style>