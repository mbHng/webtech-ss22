<template>
  <div class="home">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <div class="container" style="padding-top: 100px">
    <div class="row row-cols-3">
      <div class="col">
        <a style="text-align: left">
        <h3 class="header">
          Angebote
        </h3>
          <bt class="kopf">Collagenbehandlung:</bt>
          <p>
          Eine glättende Feuchtigkeitsbehandlung
          mit „Babyskin-Effekt“:
          - langfristige Anreicherung der Haut mit Feuchtigkeit
          - Verringerung der Trockenheut, Spannung und Schälung der Haut
          - „Plump-Effekt“ - Falten werden gefüllt und reduziert
          Angebotspreis: 85€

          Microneedling:
          Das Microneedling ist eine Revolution unter den Anti-Aging-Methoden. Es ist eine sehr effektive Hautbehandlung zur:
          - Faltenreduktion
          - Hautverjüngung
          - bei Narben sowie Schwangerschaftsstreifen
          Angebotspreis: ab 105€

          Shellack Pediküre:
          Bestehend aus:
          Fußbad, Hornhautentfernung, Nagelhautentfernung, Nägel kürzen und feilen, Shellack auftragen.
          Angebotspreis: 45€

          Mandelsäure Peeling:
          Dauer:  50-60 Minuten
          Gegen unreine Haut, Akne, großporige Haut, Pigmentverfärbungen, Falten, Straffheitsverlust
          Angebotspreis: 80€
          </p>
        </a>
      </div>
      <div class="col">Test Text</div>
      <div class="col"><card></card></div>
    </div>
  </div>
  </div>
  <h1>fknlfnaelsnfsdlkf</h1>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import card from '@/components/card'
import carousel from '@/components/carousel'
import HelloWorld from '@/components/HelloWorld.vue'

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
    HelloWorld
  }
}
</script>

<style>

b{
  text-align: left;
  text-underline: black;
}

</style>
