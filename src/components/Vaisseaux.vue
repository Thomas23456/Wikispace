<template>
    <div v-for="currency in info" class="currency" v-bind:key="currency">
        {{currency.name}}
    </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'Vaisseaux',
  props: {
    msg: String
  },
  data() {
    return {
      info : null,
    }
  },
  mounted () {
    axios
      .get('https://spacelaunchnow.me/api/3.3.0/spacecraft/?limit=30')
      .then(response => (this.info = response.data.results))
  }
}
</script>