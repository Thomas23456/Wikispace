<template>
  <h1>Nom des mecs qui vont dans l'espace</h1>
  <div v-for="currency in info" class="currency" v-bind:key="currency">
    {{ currency.name }}
    <img alt="" :src="currency.profile_image">
    <span class="lighten">
      <span v-html="currency.symbol"></span>{{ currency.results}}
    </span>
  </div>
  <div v-for="currency in inf" class="currency" v-bind:key="currency">
    {{currency.count}}
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      inf : null,
      info : null,
    }
  },
  mounted () {
    axios
      .get('https://spacelaunchnow.me/api/3.3.0/astronaut/?limit=30')
      .then(response => (this.inf = response))
      .then(response => (this.info = response.data.results))
  }
}
</script>
