<template>
    <header>

        <div class="row">
            <div class="col d-flex ps-5">

                <img src="../assets/logo-small.svg" alt="logo spotify">


            </div>

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

    .row {
        height: 80px;

        .col {
            align-items: center;

            img {
                max-width: 50px;
                height: 50px;
                
            }
        }

    }
}
</style>