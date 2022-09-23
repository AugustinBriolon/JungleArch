<template>
  <div class="hero h-screen" :style="{'background-image': `linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)), url('/images/backgrounds/${background}.png')`}">
    <Header class="fixed" />
    <div class="flex justify-center items-center flex-col h-full">
      <h1 class="text-white">{{ title }}</h1>
      <p class="subtitle text-center pb-4 text-white">Une Jungle au coeur de la défense,  lorem ipsum dolor sit amet ...</p>
      <a href="#ambiance"><button class="button button_white">Découvrir</button></a>
    </div>
  </div>
</template>

<script>
import Header from './Header.vue';

export default {
    data() {
      return {};
    },
    props: {
      title: {
        type: String,
        required: true,
      },
      background: {
        type: String,
        required: true,
      },
    },
    methods: {},
    components: { Header }
}

</script>

<style scoped lang='scss'>

.hero{
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

</style>