<script>

export default {
    data() {
        return {

        }
    },

    props: { navlinks: Array }
}
</script>

<template>
    <a v-for="link in navlinks" class="px-2" href="#">
        {{ link.name.toUpperCase() }}
    </a>
</template>

<style lang="scss" scoped>
a {
    text-decoration: none;
    color: inherit;

    &:hover {
        color: #0C7CEC;
    }
}
</style>