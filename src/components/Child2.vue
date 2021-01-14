<template>
    <div>
        <h3>Child2组件</h3>
        <hr>
        <GrandChild />
    </div>
</template>

<script>
    import GrandChild from "./GrandChild";
    export default {
        name:"Child2",
        components:{ GrandChild }
    }
</script>

<style lang="scss" scoped>

</style>