<template>
  <div class="content">
    <div id="question-block">{{ question }}</div>
    <div>Kopiera sedan texten och skicka den till dagensvibe@gmail.com!</div>
  </div>
</template>

<script>
export default {
  name: 'Formular',
  props: {
      question: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #question-block {
    width: 20vw;
    text-align: left;
    display: inline-block;
    margin: 20px;
  }
</style>