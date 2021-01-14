<template>
    <div>
        <h3>Child2组件像父组件传递数据</h3>
        <slot :data="arr"></slot>
    </div>
</template>

<script>
    export default {
       name:"Child2",
       data(){
           return {
               arr:["数学","语文","英语"]
           }
       } 
    }
</script>

<style lang="scss" scoped>

</style>