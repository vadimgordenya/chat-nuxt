<template>
  <div>
    <h1>CHAT PAGE</h1>
    <p>{{user.name}}</p>
  </div>
</template>

<script>
import { mapState } from 'vuex';
export default {
  head() {
    return {
      title: `Комната ${this.user.room}`
    }
  },
  middleware: ['chat'],
  computed: mapState(['user'])
}
</script>
