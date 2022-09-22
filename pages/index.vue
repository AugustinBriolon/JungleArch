<template>
  <div>
    <Hero />
    <Vibe />
    <SectionTitle background="hero" title="plats"/>
    <SectionTitle background="hero" title="plats"/>
    <SectionTitle background="hero" title="plats"/>
  </div>
</template>

<script>
import Hero from '../components/Hero.vue';
import Vibe from '../components/Vibe.vue';
import SectionTitle from '../components/SectionTitle.vue';
export default {
    name: "IndexPage",
    components: { Hero, Vibe, SectionTitle }
}
</script>

<style lang="scss">

@import "~/static/scss/main.scss";

</style>