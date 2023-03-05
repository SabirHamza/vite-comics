<script>

export default {
    data() {
        return {

        }
    },

    props: {
        socialimg: Array
    }
}
</script>

<template>
    <div class="d-flex">
        <div>
            <h4>FOLLOW US</h4>
        </div>

        <figure>
            <img v-for="social in socialimg" :src="'../assets/img/' + social.img" alt="">
        </figure>
    </div>
</template>

<style lang="scss" scoped>
h4 {
    color: #0C7CEC;
}
</style>