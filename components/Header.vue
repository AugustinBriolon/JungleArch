<template>
  <div class="header flex justify-between items-center w-full" ref="header">
    <nuxt-link to="/"><nuxt-img src="/images/logos/logo-jungleArch.png"></nuxt-img></nuxt-link>
    <nav>
      <ul class="text-white list-style-none flex">
        <li class="pr-10 lg:pr-20"><nuxt-link to="menu" class="links">Menu</nuxt-link></li>
        <li class="hidden lg:block pr-20"><a href="#ambiance" class="links">Ambiance</a></li>
        <li class="hidden lg:block pr-20"><a href="#plats" class="links">Plats</a></li>
        <li class="hidden lg:block "><a href="#avis" class="links">Avis</a></li>
      </ul>
    </nav>
  </div>
</template>

<script>

export default {
  data() {
    return {}
  },
  methods: {},
  mounted () {
    const header = document.querySelector('.header');
    window.addEventListener("scroll", function () {
      header.classList.toggle("sticky", window.scrollY > 200);
    });
  },
}

</script>

<style scoped lang='scss'>

.header{
  max-width: 1920px;
  padding: 0 clamp(20px, 3vw, 100px);
  z-index: 99;
  transition: .3s;
}

.sticky{
  background: rgba(0, 0, 0, 0.9);
  position: fixed;
}

</style>
