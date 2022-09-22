<template>
  <div class="header flex justify-between items-center w-full" ref="header">
    <nuxt-img src="/images/logos/logo-jungleArch.png"></nuxt-img>
    <nav>
      <ul class="text-white list-style-none flex">
        <li class="pr-20"><a href="#" class="links">Menu</a></li>
        <li class="pr-20"><a href="#" class="links">Ambiance</a></li>
        <li class="pr-20"><a href="#" class="links">Plats</a></li>
        <li><a href="#" class="links">Avis</a></li>
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

<<<<<<< HEAD
</style>
=======
.header{
  max-width: 1920px;
  padding: 0 clamp(20px, 3vw, 100px);
  z-index: 99999;
  transition: .3s;
}

.sticky{
  background: rgba(0, 0, 0, 0.6);
  position: fixed;
}

</style>
>>>>>>> dbb340c (:constrcution: Header && section title)
