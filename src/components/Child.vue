<template>
    <div>
        <h3>Child组件</h3>
        <slot name="one">有名插槽一</slot>
        <slot name="two">有名插槽二</slot>
        <slot>无名插槽</slot>
    </div>
</template>

<script>
    export default {
        name:"Child"
    }
</script>

<style lang="scss" scoped>

</style>