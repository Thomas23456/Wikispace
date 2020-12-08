<template>
  <div v-for="currency in info" :key="currency" class="container_astronaute">
    <span>
      {{ currency.name }}
      <img class="image_astronaute" :src="currency.profile_image" alt="Image astronaute"/>
      <div id="agence"></div>
    </span>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'Astronaut',
  data() {
    return {
      info : null
    }
  },
  mounted () {
    axios
      .get('https://spacelaunchnow.me/api/3.3.0/astronaut/?limit=28')
      .then(response => (this.info = response.data.results))
  }
}
</script>