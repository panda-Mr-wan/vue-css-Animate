<template>
    <div>
        <h3>Child2组件</h3>
        <button @click="changeMsg">给Child传值</button>
    </div>
</template>

<script>
    export default {
        name:"Child2",
        data(){
            return {
                message:"我是大帅哥"
            }
        },
        methods:{
            changeMsg(){
                this.$parent.$emit("myEvent",this.message)
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>