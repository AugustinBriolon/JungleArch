<template>
  <div>
    <Hero />
    <Vibe />
    <SectionTitle background="hero" title="Plats"/>
    <Plats />
    <SectionTitle background="hero" title="Avis"/>
  </div>
</template>

<script>
import Hero from '../components/Hero.vue';
import Vibe from '../components/Vibe.vue';
import SectionTitle from '../components/SectionTitle.vue';
import Plats from '../components/Plats.vue';
export default {
    name: "IndexPage",
    components: { Hero, Vibe, SectionTitle, Plats }
}
</script>

<style lang="scss">

@import "~/static/scss/main.scss";

</style>