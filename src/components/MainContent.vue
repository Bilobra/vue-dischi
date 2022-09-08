<template>
    <main class="">
        <div class="container py-5">
            <div class="mb-4">
                <label class="text-white pe-5" for="Genre">Scegli il Genere</label>

                <select class="select-genre" name="Genre" id="" v-model="ChooseGenre">
    
                    <option value="pop">Pop</option>
                    <option value="rock">Rock</option>
                    <option value="jazz">Jazz</option>
                    <option value="metal">Metal</option>
    
                </select>

            </div>
            <div class="row row-cols-2 row-cols-lg-5 row-cols-sm-3 gy-1">
                <div class="col py-4" v-for="(disk,i) in filteredGenre" :key="i">
                    <div class="card align-items-center gap-3 py-3 text-center" style="width: 16rem; height: 25rem;">
                        <img :src="disk.poster" class="card-img-top" :alt="disk.title">
                        <div class="card-body">
                            <h5 class="card-title title">{{disk.title}}</h5>
                            <p class="card-text author">{{disk.author}}</p>
                            <p class="card-text year">{{disk.year}}</p>


                        </div>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<script>
import axios from 'axios'
export default {
    data() {
        return {
            listDisk: [],
            ChooseGenre: '',
        }
    },
    computed: {
        filteredGenre() {
            return this.listDisk.filter((el) => {
                const genre = el.genre.toLowerCase()
                const find = this.ChooseGenre.toLowerCase()
                if (genre.includes(find)) {
                    return true
                }
                return false
            })
        }
    },
    created() {
        axios
            .get('https://flynn.boolean.careers/exercises/api/array/music')
            .then((res) => {
                console.log(res.data)
                this.listDisk = res.data.response;
            })
    },



}
</script>

<style lang="scss" scoped>
@import '../styles/var.scss';
@import '../styles/general.scss';

main {
    height: 100vh;
    background-color: $--dark-color;

    .select-genre{
        line-height: 20px;
        padding: 5px 8px;
        border:none;
        border-radius:4px;
        background-color: $--light-color;
        color:white;
    }
}

.card {
    background-color: $--light-color;

    .title {
        color: $--font-color;
        text-transform: uppercase;
    }

    .author,
    .year {
        font-size: 20px;
        color: #757673;
    }

    img {
        opacity: 0.7;

        &:hover {
            scale: 1.1;
            border-radius: 5px;
            border: 2px solid $--font-color;
            opacity: 1;
        }
    }
}
</style>