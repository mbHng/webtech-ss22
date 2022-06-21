<template>
  <h1>Preise und Leistungen</h1>
    <div class="prices">
      <div class="col" v-for="guest in guests" :key="guest.id">
        <h1>{{ guest.firstName }} {{guest.lastName }}</h1>
      </div>
   </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Prices',
  data () {
    return {
      guests: []
    }
  },
  methods: {},
  mounted () {
    const endUrl = process.env.VUE_APP_BACKEND_BASE_URL + '/api/v1/guests'
    const requestOptions = {
      method: 'GET',
      redirect: 'follow'
    }
    fetch(endUrl, requestOptions)
      .then(response => response.json())
      .then(result => result.forEach(guest => {
        this.guests.push(guest)
      }))
      .catch(error => console.log('error', error))
  }
}

</script>

<style scoped>

h1 {
  font-family: "Avenir Next";
  padding: 60px;
  text-align: center;
  color: black;
  font-size: 50px;
}

</style>
