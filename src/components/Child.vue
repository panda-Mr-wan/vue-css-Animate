<template>
    <div>
        <h3>Child组件</h3>
        <p>父组件中的message属性值:{{ msg }}</p>
    </div>
</template>

<script>
    export default {
        name:"Child",
        inject:['msg']
    }
</script>

<style lang="scss" scoped>

</style>