<template>
  <div class="content">
    <div :class="type">
      <h1>{{ $store.state.articles[0].header }}</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Kontakt',
  props: {
      type: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  
</style>