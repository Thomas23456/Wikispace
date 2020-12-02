<template>
  <div id="astro">
    <Astronaut />
  </div>
  <div id="vais">
    <Vaisseaux />
  </div>
  <div id="event">
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
  }
}
</script>
