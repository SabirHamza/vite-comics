<script>

import HeaderLinksApp from './links/HeaderLinksApp.vue';
import { store } from '../data/store'

export default {
    data() {
        return {
            store
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
                    <HeaderLinksApp :navlinks="store.DcComicsLinks" />
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
