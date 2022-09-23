<template>
  <div class="white-section relative" id="avis">
      <h2>Ce que pensent Nos clients</h2>
      <div class="line"></div>
      <!-- Slider Container  -->
      <div class="slider-testimonials flex gap-10" ref="sliderContainer" :style="slider">

          <!-- Card Testimonials Client -->
          <div class="card-testimonial flex flex-col" v-for="(item,i) in items" ref="sliderCard">
            <div class="flex justify-center mb-4 w-full">
                <svg v-for="(item, i) in item.stars" width="20" height="19" viewBox="0 0 20 19" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M19.3536 6.52394L13.358 5.67867L10.6778 0.407754C10.6046 0.26344 10.4841 0.146614 10.3354 0.0756018C9.96227 -0.103073 9.50887 0.0458226 9.32232 0.407754L6.64213 5.67867L0.646516 6.52394C0.481218 6.54685 0.330088 6.62244 0.214379 6.73698C0.0744931 6.87645 -0.00259025 7.06409 6.6464e-05 7.25867C0.00272317 7.45324 0.0849026 7.63884 0.228547 7.77467L4.56645 11.8773L3.5416 17.6705C3.51757 17.8053 3.53294 17.9439 3.58598 18.0706C3.63901 18.1973 3.72759 18.3071 3.84166 18.3875C3.95573 18.4678 4.09074 18.5156 4.23137 18.5253C4.37199 18.535 4.51262 18.5063 4.63729 18.4425L10 15.7074L15.3628 18.4425C15.5092 18.5181 15.6792 18.5433 15.8422 18.5158C16.2531 18.4471 16.5293 18.0691 16.4585 17.6705L15.4336 11.8773L19.7715 7.77467C19.8896 7.66242 19.9675 7.51582 19.9912 7.35547C20.0549 6.95459 19.7668 6.5835 19.3536 6.52394Z" fill="#007F7F"/>
                </svg>
            </div>
            <strong class="text-center pb-3">{{ item.client }}</strong>
            <p class="text-center">{{ item.avis }}</p>
          </div>

      </div>

      <div class="flex justify-center gap-20 mt-10">
          <svg @click="slideLeft()" class="cursor-pointer" xmlns="http://www.w3.org/2000/svg" width="40" height="40" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24"><path fill="none" stroke="#007f7f" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m15 4l-8 8l8 8"/></svg>
          <svg @click="slideRight()" class="cursor-pointer" xmlns="http://www.w3.org/2000/svg" width="40" height="40" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24"><path fill="none" stroke="#007f7f" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m8 4l8 8l-8 8"/></svg>
      </div>

  </div>
</template>

<script>

export default {
  data: function () {
      return {
          // Slider
          counter: 0,
          cardWidth: 0,

          items: [
              {
                stars: 4,
                client: "Hans .V",
                avis: "Le restaurant est constant et ne baisse pas en qualité c’est appréciable ! De nouveaux plats seraient les bienvenus pour changer un peu.",
              },
              {
                stars: 4,
                client: "Rémy .LC",
                avis: "Restaurant idéalement placé avec une très belle terrasse et une grande salle. Service rapide et correct !",
              },
              {
                stars: 4,
                client: "Stef .P",
                avis: "La décoration est soigné et agréable. Le personnel est très accueillant et aux petits soins pour vous.",
              },
              {
                stars: 4,
                client: "Dorine",
                avis: "Restaurant très sympa, le décor en conséquence et un burger veggie excellent!",
              },
              {
                stars: 4,
                client: "Élise .E",
                avis: "J'adore cet endroit, super resto et le service est très agréable. Je recommande ce restaurant de très bonne qualité, on y mange toujours très bien. Petit plus, les cocktails sont top !!",
              },
          ],
      }
  },
  methods:{
      // Function to slide Right
      slideRight: function () {
          this.counter ++
          if (this.counter >= this.$refs.sliderContainer.children.length) {
              this.counter = 0;
              this.cardWidth = 0;
          } else {
              this.cardWidth = this.$refs.sliderCard[0].offsetWidth;
              this.cardWidth = (this.cardWidth + 40) * this.counter;
          }
      },
      // Function to slide Left
      slideLeft: function () {
          this.counter --
          if (this.counter <= -1) {
              this.counter = this.$refs.sliderContainer.children.length;
              this.cardWidth = this.$refs.sliderCard[0].offsetWidth;
              this.cardWidth = ((this.cardWidth + 40) * this.counter) - (this.cardWidth + 40);
          } else {
              this.cardWidth = this.$refs.sliderCard[0].offsetWidth;
              this.cardWidth = (this.cardWidth + 40) * this.counter;
          }
      },
  },
  computed: {
      // Style to slide the card
      slider() {
          return {
              transform : `translateX(-${this.cardWidth}px)`,
              transition: "transform .5s ease-in-out",
          };
      },
  },
};

</script>

<style scoped>

    .line{
        margin: 30px 0 40px 0 !important;
    }
  .card-testimonial{
      flex-shrink: 0;
      width: 38vw;
      max-width: 700px;
      position: relative;
      padding: 50px;
      box-shadow: 0px 0px 15px 5px rgba(0,0,0,0.1);
  }
  @media screen and (max-width : 1200px){
      .card-testimonial{
          width: 70%;
          padding: 30px;
      }
  }
  @media screen and (max-width : 700px){
      .card-testimonial{
          width: 90%;
          padding: 30px;
      }
  }
</style>