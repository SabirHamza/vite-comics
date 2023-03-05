<script>
export default {
    data() {
        return {
        }
    },

    props: {
        name: String
    }
}
</script>

<template>
    <li>
        <a href="#">{{ name }}</a>
    </li>
</template>

<style lang="scss" scoped>
li {
    list-style: none;

    a {
        text-decoration: none;
        color: inherit;
        color: grey;
    }
}
</style>