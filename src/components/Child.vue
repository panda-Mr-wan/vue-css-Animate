<template>
    <div>
        <h3>Child组件</h3>
        <button @click="childMessage">给父组件传值</button>
    </div>
</template>

<script>
    export default {
        name:"Child",
        data(){
            return {
                message:"我是大帅哥"
            }
        },
        methods:{
            childMessage(){
                this.$emit("myEvent",this.message)
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>