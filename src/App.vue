<template>
  <div class="background">

    <div class="header">
      <h1>Kosmetiksalon Passion</h1>

      <carousel></carousel>

      <navbar></navbar>

      <card> </card>

      <termin></termin>
      <router-view/>
    </div>
  </div>
  <h1></h1>

  <hr style="height:2px;border-width:0;color:gray;background-color:black;">

  <h1 class="disclaimer"></h1>

  tetetetetetetetetet

</template>

<script>
import Navbar from './components/Navbar.vue'
import Carousel from '@/components/carousel'
import card from '@/components/card'
import Termin from '@/views/Termin'

export default {
  name: 'App',
  components: {
    Carousel,
    Navbar,
    // eslint-disable-next-line vue/no-unused-components
    card,
    Termin
  }
}
</script>
<style>

h1.disclaimer {
  text-align: center;

}

hr {
  margin-top: 1rem;
  margin-bottom: 1rem;
  border: 0;
  border-top: 1px solid rgba(0, 0, 0, 0.1);
}

div.background {
  background-image: url("https://img.freepik.com/free-vector/cherry-blossom-branch-with-sakura-flower-watercolor-cherry-blossom-vector-pink-sakura-flower-background-sakura-white-background-watercolor-cherry-bud-cherry-blossom-flower-blooming-vector_538213-232.jpg?w=1060");
  background-position: center;
  /*opacity: 0.5;*/
  /*https://wallpapercave.com/wp/wp7160349.png*/
}

h1 {
  font-family: "Brush Script MT";
  padding: 60px;
  text-align: center;
  color: black;
  font-size: 50px;

}

pre {
  font-family: "Brush Script MT", cursive;
  font-size: 13px;
  font-style: normal;
  font-variant: normal;
  font-weight: 400;
  line-height: 18.5714px;
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
