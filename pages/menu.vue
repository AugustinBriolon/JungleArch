<template>
  <div>
    <Hero background="background2" title="Menu"/>
    <Menu />
    <Footer />
  </div>

</template>

<script>

import Menu from "../components/Menu.vue";
import Hero from "../components/Hero.vue";
import Footer from "../components/Footer.vue";

export default {
    components: { Hero, Menu, Footer }
}
</script>

<style lang="scss">

@import "~/static/scss/main.scss";

</style>
