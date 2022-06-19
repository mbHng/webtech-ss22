<template>
  <div class="m-4">
    <div class="row g-2">
      <div class="col-12">
        <div class="input-group">
          <input type="text" class="form-control" placeholder="Vorname">
          <input type="text" class="form-control" placeholder="Nachname">
        </div>
      </div>
      <div class="col-6">
        <div class="input-group">
          <span class="input-group-text">E-Mail</span>
          <input type="text" class="form-control" placeholder="example@example.com">
        </div>
      </div>
      <div class="col-6">
        <div class="input-group">
          <input type="text" class="form-control" placeholder="Telefonnummer">
        </div>
      </div>
    </div>
  </div>

  <button type="button" class="btn btn-secondary">Submit</button>

</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Termin'
}
</script>

<style scoped>

</style>
