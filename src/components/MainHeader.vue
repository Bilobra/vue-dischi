<template>
    <header class="d-flex gap-5">


        <figure class="d-flex align-items-center m-0 ps-2">
            <img src="../assets/logo-small.svg" alt="logo spotify">

        </figure>
        <div class="d-flex align-items-center">
            <input type="text" placeholder="cerca...">
        </div>





    </header>
</template>

<script>
export default {

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

    input{
        padding: 5px 8px;
        line-height: 20px;
        border: none;
        border-radius: 3px;
        background-color: $--dark-color;
        color:white;
    }


}
</style>