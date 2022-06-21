<template>
  <div class="container">
    <div class="card" style="width: 18rem;">
      <img
        src="https://www.float-stuttgart.de/public/uploads/plugins/webshop/productsimages/1157/deluxe-rueckenmassage_0_1511091256.jpg"
        class="card-img-top" alt="...">
      <div class="card-body">
        <div class="col" v-for="guest in guests" :key="guest.id">
          <h5 class="card-title">{{ guest.firstName }} {{ guest.lastName }}</h5>
        </div>
        <p class="card-text">60 Verwöhnungsminuten zum Ausschalten vom Alltagsstress.</p>

        <form class="text-start needs-validation" id="guests-create-form" novalidate>
        <div class="m-4">
          <div class="row g-2">
            <div class="col-12">

                <label for="firstName" class="form-label">Vorname</label>
                <input type="text" class="form-control" id="firstName" v-model="firstName" required>

              <label for="lastName" class="form-label">Nachname</label>
              <input type="text" class="form-control" id="lastName" v-model="astName" required>
              </div>
            <!--            <div class="col-6">-->
            <div class="input-group">
              <!--                <span class="input-group-text">E-Mail</span>-->
              <label for="emailAdresse" class="form-label">E-Mail</label>
              <input type="text" class="form-control" id="emailAdresse" v-model="emailAdresse" required>
            </div>
          </div>
          <!--            <div class="col-6">-->
          <div class="input-group">
            <label for="telefonNummer" class="form-label">Telefonnummer</label>
            <input type="text" class="form-control" id="telefonNummer" v-model="telefonNummer" required>
            <!--              </div>-->
          </div>
          <div class="input-group">
            <label for="date" class="form-label">Datum</label>
            <input type="text" class="form-control" id="date" v-model="date" required>
          </div>

          <div v-if="this.serverValidationMessages">
            <ul>
              <li v-for="(message, index) in serverValidationMessages" :key="index" style="color: red">
                {{ message }}
              </li>
            </ul>
          </div>

          <!--        <button type="button" class="btn btn-secondary">Jetzt buchen</button> -->
          <button class="btn btn-primary me-3" type="submit" @click.prevent="createGuests">Jetzt buchen</button>
        </div>
        </form>
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
  },
  emits: ['created'],
  methods: {
    async createGuests () {
      if (this.validate()) {
        const endpoint = process.env.VUE_APP_BACKEND_BASE_URL + '/api/v1/guests'
        const headers = new Headers()
        headers.append('Content-Type', 'application/json')
        const guests = JSON.stringify({
          firstName: this.firstName,
          lastName: this.lastName,
          emailAdresse: this.emailAdresse,
          telefonNummer: this.telefonNummer,
          date: this.date
        })

        const requestOptions = {
          method: 'POST',
          headers: headers,
          body: guests,
          redirect: 'follow'
        }
        const response = await fetch(endpoint, requestOptions)
        await this.handleResponse(response)
      }
    },
    // async handleResponse (response) {
    //   if (response.ok) {
    //     this.$emit('created', response.headers.get('location'))
    //     document.getElementById('close-offcanvas').click()
    //   } else if (response.status === 400) {
    //     response = await response.json()
    //     response.errors.forEach(error => {
    //       this.serverValidationMessages.push(error.defaultMessage)
    //     })
    //   } else {
    //     this.serverValidationMessages.push('Unknown error occurred')
    //   }
    // },
    validate () {
      const form = document.getElementById('guests-create-form')
      form.classList.add('was-validated')
      return form.checkValidity()
    }
  }
}

// mounted () {
//   const endpoint = process.env.VUE_APP_BACKEND_BASE_URL + '/api/v1/guests'
//   const requestOptions = {
//     method: 'GET',
//     redirect: 'follow'
//   }
//
//   fetch(endpoint, requestOptions)
//     .then(response => response.json())
//     .then(result => result.forEach(guest => {
//       this.guests.push(guest)
//     }))
//     .catch(error => console.log('error', error))
// }
// }

</script>

<style scoped>

</style>
