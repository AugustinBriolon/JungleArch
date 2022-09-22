<template>
  <div class="section-title relative flex justify-center items-center overflow-hidden">
    <nuxt-img :src="`/images/backgrounds/${background}.png`" class="w-screen absolute z-0"/>
    <div class="w-screen h-full absolute z-10 bg-black opacity-40"></div>
    <h3 class="z-10 text-white">{{ title }}</h3>
  </div>
</template>

<script>

export default {
  data() {
    return {};
  },
  props: {
    background: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
  },
  methods: {}
}

</script>

<style scoped lang='scss'>
</style>