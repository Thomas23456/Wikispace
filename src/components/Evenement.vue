<template>
    <div></div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'Evenement',
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
      .get('https://spacelaunchnow.me/api/3.3.0/event/?limit=30')
      .then(response => (this.inf = response))
      .then(response => (this.info = response.data.results))
  }
}
</script>