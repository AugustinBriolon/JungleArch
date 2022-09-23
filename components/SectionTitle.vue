<template>
  <div class="section-title flex justify-center items-center overflow-hidden" :style="{'background-image': `linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('/images/backgrounds/${background}.png')`}">
    <h3 class="text-white">{{ title }}</h3>
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

.section-title{
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
</style>