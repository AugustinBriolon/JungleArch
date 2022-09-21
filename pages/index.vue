<template>
  <div>
    <Hero />
  </div>
</template>

<script>
import Hero from '../components/Hero.vue';
export default {
    name: "IndexPage",
    components: { Hero }
}
</script>

<style lang="scss">

@import "~/static/scss/main.scss";

</style>