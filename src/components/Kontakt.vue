<template>
  <div class="content">
    <h1>Kontakt</h1>
    <form action="">
      <input class="form-item" type="email" placeholder="Enter e-mail...">
      <textarea class="form-item" type="text" placeholder="Enter message..."></textarea>
      <input class="form-item" type="button" @submit="sendMessage" value="Send">
    </form>
  </div>
</template>

<script>
export default {
  name: 'Kontakt'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  form {
    display: inline-flex;
    flex-direction: column;
    width: 30vw;
  }
  .form-item {
    margin: 2px;
  }
</style>