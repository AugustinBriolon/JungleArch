<template>
  <div>
    
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
