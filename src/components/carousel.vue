<template class="carousel">
  <div id="carouselExampleControls" class="carousel slide" data-bs-ride="carousel">
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="https://as1.ftcdn.net/v2/jpg/02/29/86/06/1000_F_229860680_Fc2ZMSYenrMppckqE3uX2ZreE5Pj8KcE.jpg"
             class="d-block w-100" width="-10" height="360">
      </div>
      <div class="carousel-item">
        <img src="https://as2.ftcdn.net/v2/jpg/03/36/20/63/1000_F_336206326_Z6UdwfWxLz1eLzFKiBpEhIGCH5wjJK8i.jpg"
             class="d-block w-100" width="-10" height="360">
      </div>
      <div class="carousel-item">
        <img src="https://as2.ftcdn.net/v2/jpg/02/92/08/71/1000_F_292087132_IkTLYBLNJijBU0azHmO5WgMkfKct8C2G.jpg"
             class="d-block w-100" width="-10" height="360">
      </div>
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'carousel'
}
</script>

<style scoped>

</style>
