<template>
    <div>
        <div class="container">
            <img  src="../assets/1.jpg" alt="404"/>
        </div>
    </div>
</template>

<script>
    export default {
        name:"Child2"
    }
</script>

<style lang="css" scoped>
div.container{
    width:600px;
    height:200px;
    overflow:hidden
}
div.container img{
    transform:scale(1,1);
}
div.container img{
    transition:transform 0.3s ease-in 0s;
}
div.container img:hover{
    transform:scale(1.2,1.2);
    cursor:pointer;
}
</style>