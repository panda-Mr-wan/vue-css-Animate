<template>
    <div>
        <h3>Child组件</h3>
        <button @click="change">点击展示动画</button>
        <h1>An animated element</h1>
    </div>
</template>

<script>
    import "animate.css";
    export default {
        name:"Child",
        methods:{
            change(){
                let h1=document.querySelector("h1");
                h1.classList.add("animate__animated","animate__bounce");
                // 动画执行完想要做的事
                h1.addEventListener('animationend',() => {
                    alert("动画执行完毕")
                    h1.classList.remove("animate__animated","animate__bounce")
                })
            }
        }
    }
</script>

<style lang="css" scoped>

</style>