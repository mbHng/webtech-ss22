<template>
  <nav class="navbar navbar-expand-lg bg-light">
    <div class="container-fluid">
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavDropdown">
        <ul class="navbar-nav">
          <li class="nav-item">
            <!--            <a class="nav-link active" aria-current="page" href="#">Home</a>-->
            <router-link class="nav-link" to="/">Home</router-link>
          </li>
          <li class="nav-item">
            <!--            <a class="nav-link" href="#">Preise und Leistungen</a>-->
            <router-link class="nav-link" to="/preise-und-leistungen">Preise und Leistungen</router-link>
          </li>
          <li class="nav-item">
            <!--            <a class="nav-link" href="#">Termin buchen</a>-->
            <router-link class="nav-link" to="/termin-buchen">Termin buchen</router-link>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button" data-bs-toggle="dropdown" aria-expanded="false">
              Infos
            </a>
            <ul class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
              <li><router-link class="nav-link" to="/about">Über mich</router-link></li>
              <li><router-link class="nav-link" to="/impressum">Impressum und Anfahrt</router-link></li>
            </ul>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Navbar'
}
</script>

<style scoped>

</style>
