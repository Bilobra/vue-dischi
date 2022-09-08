<template>
    <header class="d-flex gap-5">


        <figure class="d-flex align-items-center m-0 ps-2">
            <img src="../assets/logo-small.svg" alt="logo spotify">

        </figure>

        <div class="">
            <label class="text-white pe-5" for="Genre">Scegli il Genere</label>

            <select class="select-genre" 
                    name="Genre" id="" 
                    v-model="search" 
                    @change="$emit('call-search',search)">

                <option class="first-option" value="">seleziona</option>
                <option value="pop">Pop</option>
                <option value="rock">Rock</option>
                <option value="jazz">Jazz</option>
                <option value="metal">Metal</option>

            </select>

        </div>






    </header>
</template>

<script>

export default {
    name: 'MainHeader',
    

    data() {
        return {
            search: '',
        }
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