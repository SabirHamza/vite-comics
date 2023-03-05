<script>
export default {
    data() {
        return {
            path: '../assets/img/'
        }
    },

    props: {
        figure: String,
        text: String
    },

}

</script>

<template>
    <div class="d-flex">
        <div>
            <img :src="path + figure" alt="">
        </div>
        <p>{{ text }}</p>
    </div>
</template>

<style></style>