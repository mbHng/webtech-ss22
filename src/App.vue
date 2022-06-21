<template>
    <div class="header">
      <h1 class="globalHeader">Kosmetiksalon Passion</h1></div>
      <carousel></carousel>
      <navbar></navbar>
  <router-view/>
</template>

<script>
import Navbar from './components/Navbar.vue'
import card from '@/components/card'
import carousel from '@/components/carousel'
import Prices from '@/views/Prices'

export default {
  name: 'App',
  components: {
    // eslint-disable-next-line vue/no-unused-components
    carousel,
    // eslint-disable-next-line vue/no-unused-components
    Navbar,
    // eslint-disable-next-line vue/no-unused-components
    card,
    // eslint-disable-next-line vue/no-unused-components
    Prices
  }
}
</script>
<style>

hr {
  margin-top: 1rem;
  margin-bottom: 1rem;
  border: 0;
  border-top: 1px solid rgba(0, 0, 0, 0.1);
}

div.header {
  background-image: url("https://img.freepik.com/free-vector/cherry-blossom-branch-with-sakura-flower-watercolor-cherry-blossom-vector-pink-sakura-flower-background-sakura-white-background-watercolor-cherry-bud-cherry-blossom-flower-blooming-vector_538213-232.jpg?w=1060");
  background-position: center;
  /*opacity: 0.5;*/
  /*https://wallpapercave.com/wp/wp7160349.png*/
}

h1{
  font-family: "Brush Script MT";
  padding: 60px;
  text-align: center;
  color: black;
  font-size: 50px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
