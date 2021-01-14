<template>
  <div>
    <h3>App组件</h3>
    <hr>
    <Child>
      <p slot="one">有名插槽一替换的内容message:{{message}}</p>
      <p slot="two">有名插槽二替换的内容</p>
      <!-- <p>无名插槽替换的内容</p> -->
    </Child>
    <hr>
    <Child2 >
      <template slot-scope="props">
        <ul>
          <li  v-for="(value,index) in props.data" :key="index">
            {{value}}
          </li>
        </ul>
      </template>
    </Child2>
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
        message:"我是大帅哥"
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>