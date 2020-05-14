<template>
  <div class="content">
    <h1>{{ $route.params.artikel }}</h1>
  </div>
</template>

<script>
export default {
  name: 'Kontakt'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #email {
    margin: 30vh;
    font-size: 1.5em;
  }
</style>