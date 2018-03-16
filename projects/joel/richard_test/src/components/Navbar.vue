<template>
  <div class="navbar">
    <router-link v-bind:to="'/designers'" class="navlink navlink-left">Designers</router-link>
    <router-link v-bind:to="'/contact'" class="navlink navlink-left">Contact</router-link>
    <router-link v-bind:to="'/'"><img class="main-logo" src="../assets/wwd-logo-blue.png"></router-link>
    <router-link v-bind:to="'/about'" class="navlink navlink-right">About</router-link>
    <p class="navlink navlink-right">Search</p>
  </div>
</template>

<script>
export default {
  name: 'navbar'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}

a {
  text-decoration: none;
}

.navbar {
  width: 100%;
  height: 75px;
  background-color: #E4EACE;
  margin: auto;
  text-align: center;
  padding-top: 25px;
}

.main-logo {
  display: inline-block;
  width: 150px;
  margin-top: -20px;
}

.navlink {
  display: inline-block;
  width: 175px;
  font-size: 30px;
  color: #2B3D4E;
  border-bottom: 3px solid #2B3D4E;
  font-weight: 600;
  vertical-align: top;
  transition: 0.3s;
  text-transform: uppercase;
}

.navlink-left {
  margin: 0px 5vw 0px 0px;
  text-align: right;
  padding: 0px 0px 0px 50px;
}

.navlink-right {
  margin: 0px 0px 0px 5vw;
  text-align: left;
  padding: 0px 50px 0px 0px;
}



.navlink:hover {
  color: #004177;
  border-bottom: 3px solid #004177;
  transition: 0.3s;
}
</style>
