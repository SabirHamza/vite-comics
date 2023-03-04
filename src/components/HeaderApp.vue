<script>

import HeaderLinksApp from './HeaderLinksApp.vue';

export default {
    data() {
        return {
            links: [
                {
                    name: 'CHARACTERS'
                },
                {
                    name: 'COMICS'
                },
                {
                    name: 'MOVIE'
                },
                {
                    name: 'TV'
                },
                {
                    name: 'GAMES'
                },
                {
                    name: 'COLECTIBLES'
                },
                {
                    name: 'VIDEOS'
                },
                {
                    name: 'FANS'
                },
                {
                    name: 'NEWS'
                },
                {
                    name: 'SHOP'
                },
            ]
        }
    },

    components: { HeaderLinksApp }
}
</script>

<template>
    <header>
        <div class="container">
            <div class="row justify-content-between">
                <div class="col-auto">
                    <img class="" src="../assets/img/dc-logo.png" alt="">
                </div>
                <div class="col-auto">
                    <HeaderLinksApp :navlinks="links" />
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
.col-auto {
    display: flex;
    justify-content: center;
    align-items: center;

    img {
        padding: 1rem 0;
        width: 70%;
    }
}
</style>
