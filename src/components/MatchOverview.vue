<template>
  <div class="app-content__match-overview">
    <Matches />
  </div>
</template>

<script>

import Matches from './Matches'

export default {
  name: 'MatchOverview',
  components: {
    Matches,
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style scoped>

</style>
