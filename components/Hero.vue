<template>
  <div class="hero h-screen">
    <Header class="fixed" />
    <div class="flex justify-center items-center flex-col h-full">
      <h1 class="text-white">Jungle Arch</h1>
      <p class="subtitle text-center pb-4 text-white">Une Jungle au coeur de la défense,  lorem ipsum dolor sit amet ...</p>
      <button>Découvrir</button>
    </div>
  </div>
</template>

<script>
import Header from './Header.vue';

export default {
    data() {
        return {};
    },
    methods: {},
    components: { Header }
}

</script>

<style scoped lang='scss'>
.hero{
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('/images/backgrounds/hero.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
</style>