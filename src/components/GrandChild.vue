<template>
    <div>
        <h3>GrandChild组件</h3>
        <p>祖先元素传递过来的message属性值:{{ msg }}</p>
        <button @click="changeMsg2">点击改变祖先元素的message值</button>
        <p>祖先元素传递过来的name属性值:{{ obj.name | checkName }}</p>
        <button @click="changeMsg3">点击改变祖先元素的name值</button>
    </div>
</template>

<script>
    export default {
        name:"GrandChild",
        inject:['msg','change','obj'],
        data(){
            return {
                data:"我是大好人"
            }
        },
        methods:{
            changeMsg2(){
                this.change(this.data)
            },
            changeMsg3(){
                this.obj.name="jarry"
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>