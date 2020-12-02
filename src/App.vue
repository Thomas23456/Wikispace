<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <div id="astro">
    <HelloWorld />
  </div>
  <div id="vais">
    <Vaisseaux />
  </div>
  <div>
    <Evenement />
  </div>
</template>
<script>
import HelloWorld from './components/HelloWorld.vue'
import Vaisseaux from './components/Vaisseaux.vue'
import Evenement from './components/Evenement.vue'

export default {
  name: 'App',
  components: {
    HelloWorld, Vaisseaux, Evenement
  }
}
</script>
