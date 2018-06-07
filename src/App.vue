<template>
  <div id="app">
    
    <h1>Witaj w systemie do zapisow na zajecia!!</h1>
   

    <div v-if="authenticatedUsername">   
    <h2> Witaj {{authenticatedUsername}}
      <button  @click="logout()">Wyloguj</button>
      <meeting-page></meeting-page>
    </h2>  

    </div> 

    <div v-else>
     <login-form @login="login($event)"></login-form>
    </div>

  </div>

 </template>
 
 <script>

 import "milligram"
 import LoginForm from "./LoginForm";
 import MeetingPage from "./meetings/MeetingPage"

 export default {
 name: "app",

 components: {LoginForm, MeetingPage},
 data() {
     return {
     authenticatedUsername: '',   
  };
 },
 methods: { 
    login(username) {
    this.authenticatedUsername = username;
  },  
   logout() {
     this.authenticatedUsername = '';
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
  text-align: left;
}

h2 {
  font-weight: normal; 
  text-align: left;
}

button {
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
