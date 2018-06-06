<template>
  <div id="app">
    <h1>Witaj w systemie do zapisow na zajecia!!</h1>
   
  <div v-if="logged">    
   <h2>Twój e-mail to:  {{ email }}</h2> 
      <button @click="logout()">Wyloguj</button>
      </div>

 <div v-else>
  <h2> Zaloguj sie emailem  <input type="email" v-model="email"> </h2>
      <button @click="login()">Wchodzę</button>
   </div>
</div>
 </template>
 
 <script>
 export default {
 name: "app",
 data() {
     return {
    email: '',
    logged: false
  };
 },
 methods: {
  login() {
    this.logged = true;
  },
   logout() {
     this.logged = false;
     }
   }

};
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
