<template>
    <div>
        <h3>Child组件</h3>
        <p>{{200+numChild}}</p>
        <p>{{message}}</p>
        <p>{{data}}</p>
        <p>{{propF}}</p>
    </div>
</template>

<script>
    export default {
        name:"Child",
        // props:['numChild']
        props:{
            numChild:Number,
            message:{
                type:String,
                required:true
            },
            data:[Number,String],
            propF:{
                validator(value){
                    return value>20
                }
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>