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
      info : null,
    }
  },
  mounted () {
    axios
      .get('https://spacelaunchnow.me/api/3.3.0/event/?limit=30')
      .then(response => (this.info = response.data.results))
  }
}
</script>