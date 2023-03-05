<script>
export default {
    props: {
        comicob: Object
    }
}
</script>

<template>
    <div class="col-2">
        <img :src="comicob.thumb" alt="">
        <span>{{ comicob.series }}</span>
    </div>
</template>

<style lang="scss" scoped></style>