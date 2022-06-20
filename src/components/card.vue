<template>
  <div class="container">
    <div class="card" style="width: 18rem;">
      <img
        src="https://www.float-stuttgart.de/public/uploads/plugins/webshop/productsimages/1157/deluxe-rueckenmassage_0_1511091256.jpg"
        class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">Rückenmassage 60 Min.</h5>
        <p class="card-text">60 Verwöhnungsminuten zum Ausschalten vom Alltagsstress.</p>

        <div class="m-4">
          <div class="row g-2">
            <div class="col-12">

              <div class="input-group">
                <input type="text"  class="form-control" placeholder="Vorname">
                <input type="text" class="form-control" placeholder="Nachname">
              </div>
            </div>
            <!--            <div class="col-6">-->
            <div class="input-group">
              <!--                <span class="input-group-text">E-Mail</span>-->
              <input type="text" class="form-control" placeholder="example@example.com">
            </div>
          </div>
          <!--            <div class="col-6">-->
          <div class="input-group">
            <input type="text" class="form-control" placeholder="Telefonnummer">
            <!--              </div>-->
          </div>
          <div class="input-group">
            <input type="text" class="form-control" placeholder="Datum">
          </div>

          <!--        <button type="button" class="btn btn-secondary">Jetzt buchen</button> -->
          <a href="#" class="btn btn-primary">Jetzt buchen!</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

  // eslint-disable-next-line vue/multi-word-component-names
  name: 'card',
  data () {
    return {
      guests: []
    }
  },

  mounted () {
    const endpoint = process.env.VUE_APP_BACKEND_BASE_URL + '/api/v1/guest'
    const requestOptions = {
      method: 'GET',
      redirect: 'follow'
    }

    fetch(endpoint, requestOptions)
      .then(response => response.json())
      .then(result => result.forEach(guest => {
        this.guests.push(guest)
      }))
      .catch(error => console.log('error', error))
  }
}

</script>

<style scoped>

</style>
