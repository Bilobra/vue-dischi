<template>
    <main class="py-5">
        <div class="container mx-auto">
            <div class="row">
                <div class="col" v-for="(disk,i) in listDisk" :key="i">
                    <div class="card" style="width: 18rem;">
                        <img :src="disk.poster" class="card-img-top" :alt="disk.title">
                        <div class="card-body">
                            <h5 class="card-title">{{disk.title}}</h5>
                            <p class="card-text">{{disk.author}}</p>
                            <p class="card-text">{{disk.year}}</p>


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
        }
    },
    created() {
        axios
            .get('https://flynn.boolean.careers/exercises/api/array/music')
            .then((res) => {
                console.log(res.data)
                this.listDisk = res.data;
            })
    }


}
</script>

<style lang="scss" scoped>
@import '../styles/var.scss';
@import '../styles/general.scss';

main {
    height: 100vh;
    background-color: $--dark-color;
}
</style>