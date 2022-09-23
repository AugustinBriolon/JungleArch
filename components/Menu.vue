<template>
  <div>
    <h1>Menu</h1>
    <div>
      <h2>Entrees</h2>
      <div class="line"></div>
    </div>
    <div>
      <h2>Plats</h2>
      <div class="line"></div>
    </div>
    <div>
      <h2>Desserts</h2>
      <div class="line"></div>
    </div>
    <div>
      <h2>Vins</h2>
      <div class="line"></div>
    </div>
    <div>
      <h2>Cocktails</h2>
      <div class="line"></div>
    </div>
    <div>
      <h2>Alcools</h2>
      <div class="line"></div>
    </div>
    <div>
      <h2>Boissons Fraiches</h2>
      <div class="line"></div>
    </div>
    <div>
      <h2>Boissons CHaudes</h2>
      <div class="line"></div>
    </div>
  </div>
  
</template>

<script>

export default {
  data() {
    return {
      menu: [
        { name: String },
        { price: Number },
        { description: String }
      ],
    }
  },
  methods: {
    asyncData: async function() {
      const APIkey = 'keyBC7Fc0yhZ7VpP1';
      const api = 'https://api.airtable.com/v0/appUVoiNznbBo9b6v/Plats?api_key='+APIkey
      const data = await fetch(api).then((response) => {
        return response.json()
      })
      return data.records;
    },
    fetchApiResponse: function() {
      console.log(this.asyncData())
    }
  },
  mounted() {
    this.asyncData()
  }

}
</script>

<style lang="scss"></style>
