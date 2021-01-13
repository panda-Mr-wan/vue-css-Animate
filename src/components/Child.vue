<template>
    <div>
        <h3>Child组件</h3>
        <p>通过父组件自定义事件传递过来的Child2的值:{{message}}</p>
    </div>
</template>

<script>
    export default {
        name:"Child",
        data(){
            return {
                message:""
            }
        },
        mounted(){
            this.$on("myEvent",msg => {
                this.message=msg;
            })
        }
    }
</script>

<style lang="scss" scoped>

</style>