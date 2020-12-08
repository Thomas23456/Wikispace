<template>
  <div id="menu">
    <ul class="liste_options">
      <a href="#" id="astro_link" class="selected" v-on:click="link('astro')"><li>Astronautes</li></a>
      <a href="#" id="vais_link" class="" v-on:click="link('vais')"><li>Vaisseaux</li></a>
      <a href="#" id="event_link" class="" v-on:click="link('event')"><li>Evénements</li></a>
    </ul>
  </div>
  <div id="astro" class="">
    <Astronaut />
  </div>
  <div id="vais" class="no_selected">
    <Vaisseaux />
  </div>
  <div id="event" class="no_selected">
    <Evenement />
  </div>

</template>
<script>
import Astronaut from './components/Astronaut.vue'
import Vaisseaux from './components/Vaisseaux.vue'
import Evenement from './components/Evenement.vue'

export default {
  name: 'App',
  components: {
    Astronaut, Vaisseaux, Evenement
  },
  methods: {
    link: function (message) {
      if(message == 'astro'){
        alert('astro')
      }
      else if(message == 'vais'){
        alert('vais')
      }
      else if(message == 'event'){
        alert('event')
      }
    }
  }
}

</script>
