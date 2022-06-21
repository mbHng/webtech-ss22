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
      guests: [
        {
          id: 1,
          telefonNummer: '1243234788',
          lastName: 'Max',
          firstName: 'Mustermann',
          emailAdresse: 'testguest@htw.de',
          date: '21.05.2020 13:23'
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>
