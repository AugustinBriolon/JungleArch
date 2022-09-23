<template>
  <div>


    <div class="menu-section flex flex-col justify-center">
      <MenuTitle title="Carte du Jour" />

      <div class="lg:grid lg:grid-cols-2 lg:gap-10">
        <div class="menu-card">
          <h4 class="lg:mx-12 mb-12">Plats du jour</h4>
          <div
            class="flex flex-row justify-between"
            v-for="(menu, i) in menuDuJour"
            :key="i"
          >
            <div class="mb-8">
              <h5 class="mb-3">{{ menu.Name }}</h5>
              <p>{{ menu.Description }}</p>
            </div>
            <h5 class="menu-card-price">{{ menu.Price }} €</h5>
          </div>
        </div>

        <div class="menu-card">
          <h4 class="lg:mx-12 mb-12">Dessert du jour</h4>
          <div
            class="flex flex-row justify-between"
            v-for="(menu, i) in menuDuJourDesssert"
            :key="i"
          >
            <div class="mb-8">
              <h5 class="mb-3">{{ menu.Name }}</h5>
              <p>{{ menu.Description }}</p>
            </div>
            <h5 class="menu-card-price">{{ menu.Price }} €</h5>
          </div>
        </div>
      </div>
    </div>


    <div class="menu-section flex flex-col justify-center">
      <MenuTitle title="Entrees" />

      <div class="lg:grid lg:grid-cols-2 lg:gap-10">
        <div class="menu-card">
          <h4 class="lg:mx-12 mb-12">A Paratager</h4>
          <div
            class="flex flex-row justify-between"
            v-for="(menu, i) in menuShared"
            :key="i"
          >
            <div class="mb-8">
              <h5 class="mb-3">{{ menu.Name }}</h5>
              <p>{{ menu.Description }}</p>
            </div>
            <h5 class="menu-card-price">{{ menu.Price }} €</h5>
          </div>
        </div>
        <div class="menu-card">
          <h4 class="lg:mx-12 mb-12">Salades</h4>
          <div
            class="flex flex-row justify-between"
            v-for="(menu, i) in menuSalad"
            :key="i"
          >
            <div class="mb-8">
              <h5 class="mb-3">{{ menu.Name }}</h5>
              <p>{{ menu.Description }}</p>
            </div>
            <h5 class="menu-card-price">{{ menu.Price }} €</h5>
          </div>
        </div>
      </div>
    </div>


    <div class="menu-section flex flex-col justify-center">
      <MenuTitle title="Plats" />

      <div class="lg:grid lg:grid-cols-2 lg:gap-10">
        <div class="menu-card">
          <h4 class="lg:mx-12 mb-12">Plats</h4>
          <div
            class="flex flex-row justify-between"
            v-for="(menu, i) in menuPlat"
            :key="i"
          >
            <div class="mb-8">
              <h5 class="mb-3">{{ menu.Name }}</h5>
              <p>{{ menu.Description }}</p>
            </div>
            <h5 class="menu-card-price">{{ menu.Price }} €</h5>
          </div>
        </div>

        <div class="menu-card">
          <h4 class="lg:mx-12 mb-12">Burgers</h4>
          <div
            class="flex flex-row justify-between"
            v-for="(menu, i) in menuBurger"
            :key="i"
          >
            <div class="mb-8">
              <h5 class="mb-3">{{ menu.Name }}</h5>
              <p>{{ menu.Description }}</p>
            </div>
            <h5 class="menu-card-price">{{ menu.Price }} €</h5>
          </div>
        </div>
      </div>
    </div>


    <div class="menu-section flex flex-col justify-center">
      <MenuTitle title="Desserts" />

      <div class="lg:grid lg:grid-cols-2 lg:gap-10">
        <div class="menu-card">
          <div
            class="flex flex-row justify-between"
            v-for="(menu, i) in menuDessert"
            :key="i"
          >
            <div class="mb-8">
              <h5 class="mb-3">{{ menu.Name }}</h5>
              <p>{{ menu.Description }}</p>
            </div>
            <h5 class="menu-card-price">{{ menu.Price }} €</h5>
          </div>
        </div>
      </div>
    </div>

    <div class="menu-section flex flex-col justify-center">
      <MenuTitle title="Happy Hour" />

      <div class="lg:grid lg:grid-cols-2 lg:gap-10">
        <div class="menu-card">
          <div
            class="flex flex-row justify-between"
            v-for="(menu, i) in menuHappyHour"
            :key="i"
          >
            <div class="mb-8">
              <h5 class="mb-3">{{ menu.Name }}</h5>
              <p>{{ menu.Description }}</p>
            </div>
            <h5 class="menu-card-price">{{ menu.Price }} €</h5>
          </div>
        </div>
      </div>
    </div>


    <div class="menu-section flex flex-col justify-center">
      <MenuTitle title="Vins" />
    </div>


    <div class="menu-section flex flex-col justify-center">
      <MenuTitle title="Cocktails" />

      <div class="lg:grid lg:grid-cols-2 lg:gap-10">
        <div class="menu-card">
          <h4 class="lg:mx-12 mb-12">Cocktails</h4>

          <div
            class="flex flex-row justify-between"
            v-for="(menu, i) in menuCocktail"
            :key="i"
          >
            <div class="mb-8">
              <h5 class="mb-3">{{ menu.Name }}</h5>
              <p>{{ menu.Description }}</p>
            </div>
            <h5 class="menu-card-price">{{ menu.Price }} €</h5>
          </div>
        </div>

        <div class="menu-card">
          <h4 class="lg:mx-12 mb-12">Jungle Cocktails</h4>

          <div
            class="flex flex-row justify-between"
            v-for="(menu, i) in menuCocktailJungle"
            :key="i"
          >
            <div class="mb-8">
              <h5 class="mb-3">{{ menu.Name }}</h5>
              <p>{{ menu.Description }}</p>
            </div>
            <h5 class="menu-card-price">{{ menu.Price }} €</h5>
          </div>
        </div>
      </div>
    </div>


    <div class="menu-section flex flex-col justify-center">
      <MenuTitle title="Alcools" />
    </div>


    <div class="menu-section flex flex-col justify-center">
      <MenuTitle title="Boissons Fraiches" />
    </div>


    <div class="menu-section flex flex-col justify-center">
      <MenuTitle title="Boissons Chaudes" />
    </div>


  </div>

</template>

<script>
import MenuTitle from "./MenuTitle.vue";

export default {
  data() {
    return {
      menuDuJour: [],
      menuDuJourDesssert: [],
      menuPlat: [],
      menuShared: [],
      menuSalad: [],
      menuBurger: [],
      menuDessert: [],
      menuHappyHour: [],
      menuVinRed: [],
      menuVinWhite: [],
      menuRose: [],
      menuChampagne: [],
      menuCocktail: [],
      menuCocktailJungle: [],
      menuSoft: [],
    };
  },
  methods: {
    dailyData: async function () {
      const APIkey = process.env.AIRTABLE_API_KEY;
      const api =
        "https://api.airtable.com/v0/appUVoiNznbBo9b6v/Dessert%20du%20Jour?api_key=keyBC7Fc0yhZ7VpP1";
      const data = await fetch(api).then((response) => {
        return response.json();
      });
      data.records.forEach((record) => {
        this.menuDuJourDesssert.push(record.fields);
      });
    },
    dailyDessertData: async function () {
      const APIkey = process.env.AIRTABLE_API_KEY;
      const api =
        "https://api.airtable.com/v0/appUVoiNznbBo9b6v/Plat%20du%20Jour?api_key=keyBC7Fc0yhZ7VpP1";
      const data = await fetch(api).then((response) => {
        return response.json();
      });
      data.records.forEach((record) => {
        this.menuDuJour.push(record.fields);
      });
    },
    platsData: async function () {
      const APIkey = process.env.AIRTABLE_API_KEY;
      const api =
        "https://api.airtable.com/v0/appUVoiNznbBo9b6v/Plats?api_key=keyBC7Fc0yhZ7VpP1";
      const data = await fetch(api).then((response) => {
        return response.json();
      });
      data.records.forEach((record) => {
        this.menuPlat.push(record.fields);
      });
    },
    sharedData: async function () {
      const APIkey = process.env.AIRTABLE_API_KEY;
      const api =
        "https://api.airtable.com/v0/appUVoiNznbBo9b6v/A%20Partager?api_key=keyBC7Fc0yhZ7VpP1";
      const data = await fetch(api).then((response) => {
        return response.json();
      });
      data.records.forEach((record) => {
        this.menuShared.push(record.fields);
      });
    },
    saladData: async function () {
      const APIkey = process.env.AIRTABLE_API_KEY;
      const api =
        "https://api.airtable.com/v0/appUVoiNznbBo9b6v/Salades?api_key=keyBC7Fc0yhZ7VpP1";
      const data = await fetch(api).then((response) => {
        return response.json();
      });
      data.records.forEach((record) => {
        this.menuSalad.push(record.fields);
      });
    },
    burgerData: async function () {
      const APIkey = process.env.AIRTABLE_API_KEY;
      const api =
        "https://api.airtable.com/v0/appUVoiNznbBo9b6v/Burger?api_key=keyBC7Fc0yhZ7VpP1";
      const data = await fetch(api).then((response) => {
        return response.json();
      });
      data.records.forEach((record) => {
        this.menuBurger.push(record.fields);
      });
    },
    dessertData: async function () {
      const APIkey = process.env.AIRTABLE_API_KEY;
      const api =
        "https://api.airtable.com/v0/appUVoiNznbBo9b6v/Desserts?api_key=keyBC7Fc0yhZ7VpP1";
      const data = await fetch(api).then((response) => {
        return response.json();
      });
      data.records.forEach((record) => {
        this.menuDessert.push(record.fields);
      });
    },
    happyHourData: async function () {
      const APIkey = process.env.AIRTABLE_API_KEY;
      const api =
        "https://api.airtable.com/v0/appUVoiNznbBo9b6v/Happy%20Hours?api_key=keyBC7Fc0yhZ7VpP1";
      const data = await fetch(api).then((response) => {
        return response.json();
      });
      data.records.forEach((record) => {
        this.menuHappyHour.push(record.fields);
      });
    },
    coktailData: async function () {
      const APIkey = process.env.AIRTABLE_API_KEY;
      const api =
        "https://api.airtable.com/v0/appUVoiNznbBo9b6v/Cocktails%20classiques?api_key=keyBC7Fc0yhZ7VpP1";
      const data = await fetch(api).then((response) => {
        return response.json();
      });
      data.records.forEach((record) => {
        this.menuCocktail.push(record.fields);
      });
    },
    jungleCoktailData: async function () {
      const APIkey = process.env.AIRTABLE_API_KEY;
      const api =
        "https://api.airtable.com/v0/appUVoiNznbBo9b6v/Jungle%20Cocktails?api_key=keyBC7Fc0yhZ7VpP1";
      const data = await fetch(api).then((response) => {
        return response.json();
      });
      data.records.forEach((record) => {
        this.menuCocktailJungle.push(record.fields);
      });
    },
  },
  mounted() {
    this.dailyData();
    this.dailyDessertData();
    this.platsData();
    this.sharedData();
    this.saladData();
    this.burgerData();
    this.dessertData();
    this.happyHourData();
    this.coktailData();
    this.jungleCoktailData();
  },
  components: { MenuTitle },
};
</script>

<style lang="scss" scoped>
.menu-card {
  width: 100%;
  padding: clamp(20px, 7vh, 10rem) clamp(20px, 6vw, 8rem);
  margin: 5vh auto;
  box-shadow: 0px 0px 15px 5px rgba(0, 0, 0, 0.1);
  height: fit-content;

  &-price {
    min-width: fit-content;
    margin-left: 3vw;
  }
}
</style>
