<template>
    <header class="d-flex gap-5">


        <figure class="d-flex align-items-center m-0 ps-2">
            <img src="../assets/logo-small.svg" alt="logo spotify">

        </figure>
       





    </header>
</template>

<script>

export default {
    name:'MainHeader',
    components:{
        
    },
    data(){
        return{
            
        }
    },
    props: {
       
    },
    
}
</script>

<style lang="scss" scoped>
@import '../styles/var.scss';


header {
    background-color: $--light-color;
    height: 80px;
    padding: 0 20px;

    img {
        max-width: 50px;
        height: 50px;

    }

    


}
</style>