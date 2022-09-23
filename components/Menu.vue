<template>
  <div>
    <div class="menu-section flex flex-col justify-center">
      <MenuTitle title="Entrees"/>
      <div class="lg:grid lg:grid-cols-2 lg:gap-10">
        <div class="menu-card">
          <h4 class="lg:mx-12 mb-12">A Partager</h4>
          <div class="flex flex-row justify-between" v-for="(partage,i) in partages">
            <div class="mb-8">
              <h5 class="mb-3">{{ partage.title }}</h5>
              <p>{{ partage.description }}</p>
            </div>
            <h5 class="menu-card-price">{{ partage.price }} €</h5>
          </div>
        </div>
        <div class="menu-card">
          <h4 class="mx-12 mb-12">Salades</h4>
          <div class="flex flex-row justify-between" v-for="(salade,i) in salades">
            <div class="mb-8">
              <h5 class="mb-3">{{ salade.title }}</h5>
              <p>{{ salade.description }}</p>
            </div>
            <h5 class="menu-card-price">{{ salade.price }} €</h5>
          </div>
        </div>
      </div>
    </div>
    <div>
      <MenuTitle title="Plats"/>
    </div>
    <div>
      <MenuTitle title="Desserts"/>
    </div>
    <div>
      <MenuTitle title="Vins"/>
    </div>
    <div>
      <MenuTitle title="Cocktails"/>
    </div>
    <div>
      <MenuTitle title="Alcools"/>
    </div>
    <div>
      <MenuTitle title="Boissons Fraiches"/>
    </div>
    <div>
      <MenuTitle title="Boissons Chaudes"/>
    </div>
  </div>
</template>

<script>
import MenuTitle from './MenuTitle.vue';

export default {
    data() {
        return {
            menu: [
                { name: String },
                { price: Number },
                { description: String }
            ],
            partages: [
              {
                  title: "PLANCHE TAPAS",
                  description: "beignets de calamars, nems de poulet, bouchées de Camembert, sticks de mozzarella et onion rings",
                  price: "14",
              },
              {
                  title: "PLANCHE CHARCUTERIE, FROMAGES OU MIXTE",
                  description: "",
                  price: "20",
              },
              {
                  title: "ASSIETTE DE FRITES MAISON",
                  description: "",
                  price: "5,50",
              },
              {
                  title: "PLANCHE VEGGIE",
                  description: "houmous maison, crudités, crème ciboulette, galette patates douces",
                  price: "20",
              },
          ],
          salades: [
              {
                  title: "LA CESAR",
                  description: "poulet croustillant, salade romaine, croûtons, copeaux de parmesan, œuf, tomates et véritable sauce cæsar",
                  price: "17,50",
              },
              {
                  title: "TARTARE DE MELON ET JAMBON SERRANO",
                  description: "mesclun, roquette, tomates, parmesan",
                  price: "17,50",
              },
              {
                  title: "GREEN BOWL",
                  description: "kiwi, avocat, concombre, courgettes, tomates vertes, fêta marinée aux herbes, graines de courge, vinaigrette au kiwi",
                  price: "18",
              },
              {
                  title: "ANTIPASTI",
                  description: "courgettes, aubergines, poivrons, artichauts marinés, tomates, câpres à queue, pignons de pin, mozzarelle di buffala",
                  price: "18",
              },
              {
                  title: "POKE BOWL THON",
                  description: "(version vegan 17.00€) thon, avocat, radis, edamame, carottes, concombre, mangue, tomates, riz vinaigré",
                  price: "18,50",
              },
              {
                  title: "SALADE DE CHÈVRE",
                  description: "billes de chèvre frais aux fruits secs, poitrine de cochon grillée, tomates, mesclun, pommes Granny Smith, vinaigrette au miel",
                  price: "18,50",
              },
          ],
        };
    },
    methods: {
        asyncData: async function () {
            const APIkey = "keyBC7Fc0yhZ7VpP1";
            const api = "https://api.airtable.com/v0/appUVoiNznbBo9b6v/Plats?api_key=" + APIkey;
            const data = await fetch(api).then((response) => {
                return response.json();
            });
            return data.records;
        },
        fetchApiResponse: function () {
            console.log(this.asyncData());
        }
    },
    mounted() {
        this.asyncData();
    },
    components: { MenuTitle }
}
</script>

<style lang="scss" scoped>

  .menu-card {
    width: 100%;
    padding: clamp(20px, 7vh, 10rem) clamp(20px, 6vw, 8rem);
    margin: 5vh auto;
    box-shadow: 0px 0px 15px 5px rgba(0,0,0,0.1);
    height: fit-content;

    &-price {
      min-width: fit-content;
      margin-left: 3vw;
    }
  }

</style>
