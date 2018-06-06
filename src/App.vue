<template>
  <div id="app">
    <h1>Witaj w systemie do zapisow na zajecia!!</h1>

    <h4> 
      <div v-if="email.length < 10">Ale masz krótki adres!</div>
      <div v-else-if="email.length < 15">Twój adres e-mail jest w sam raz.</div>
      <div v-else>Twój adres e-mail jest stanowczo za długi.</div>
    </h4>
    <h2>
      Zaloguj sie emailem  <input type="email" v-model="email"> 

    <button @click="alertMyEmail()">Wchodze </button> 

    </h2>
     
  </div>

</template>



<script>
export default {
data() {
  return {
    email: ''
  };
},
methods: {
  alertMyEmail() {
    alert(this.email);
  }
}
}

</script>



<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1 {
  font-weight: normal;
}

h2 {
  font-weight: normal; 
  text-align: left;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
