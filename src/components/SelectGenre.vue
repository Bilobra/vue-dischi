<template>
    <div>
        <select name="genre" id="" v-model="chooseGenre">
            <option value="all">all</option>
            <option value="pop">Pop</option>
            <option value="rock">Rock</option>
            <option value="jazz">Jazz</option>
            <option value="metal">Metal</option>
        </select>
    </div>
</template>

<script>
    export default{
        name: 'SelectGenre',

        data(){
            return{
                chooseGenre : "",
            }
        }
    }
</script>

<style lang="scss" scoped>
    
</style>