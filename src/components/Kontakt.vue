<template>
  <div class="content">
    <!-- <div id="email">dagensvibe@gmail.com</div> -->
    <h2>Här kan du ställa en fråga</h2>
    <textarea v-model="question" placeholder="Vad vill du fråga om?" id="question-input" cols="30" rows="5"></textarea>
    <Formular :question="question"></Formular>
  </div>
</template>

<script>
import Formular from './Formular.vue'

export default {
  name: 'Kontakt',
  components: {
    Formular
  },
  computed: {
    question: {
      get() {
        return this.$store.state.question
      },
      set(someQuestion) {
        this.$store.commit('setQuestion', someQuestion)
        // this.$store.state.question = someQuestion
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #email {
    margin: 30vh;
    font-size: 1.5em;
    font-weight: bold;
  }
  #question-input {
    width: 15vw;
  }
</style>