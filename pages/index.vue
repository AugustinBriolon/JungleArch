<template>
  <div>
    <Hero background="background1" title="Jungle Arch"/>
    <Vibe />
    <SectionTitle background="background3" title="Plats"/>
    <Plats />
    <SectionTitle background="background4" title="Avis"/>
    <Testimonials />
    <Footer />
  </div>
</template>

<script>

import Hero from '../components/Hero.vue';
import Vibe from '../components/Vibe.vue';
import SectionTitle from '../components/SectionTitle.vue';
import Plats from '../components/Plats.vue';
import Testimonials from '../components/Testimonials.vue';
import Footer from '../components/Footer.vue';

export default {
    name: "IndexPage",
    components: { Hero, Vibe, SectionTitle, Plats, Testimonials, Footer }
}

</script>

<style lang="scss">

@import "~/static/scss/main.scss";

</style>