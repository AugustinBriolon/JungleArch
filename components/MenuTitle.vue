<template>
    <div class="menu-title-container">
        <h2>{{ title }}</h2>
        <div class="line"></div>
    </div>
</template>

<script>

export default {
    data() {
        return {};
    },
    props: {
        title: {
            type: String,
            required: true,
        },
    },
    methods: {}
}

</script>

<style lang="scss" scoped>
    .menu-title-container {
        width: fit-content;
    }
</style>