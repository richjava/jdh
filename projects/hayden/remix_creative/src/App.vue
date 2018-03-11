<template>
  <div id="app">
    <header>
      <div class="logo">
        <img src="./assets/remix-creative-logo.png" alt="">
      </div><!-- / logo -->
      <nav>
        <router-link v-bind:to="'/'">Home</router-link>
        <router-link v-bind:to="'/designers'">Our Designers</router-link>
        <router-link v-bind:to="'/about'">About</router-link>
      </nav>
    </header>

    <div id="page">
      <router-view></router-view>
    </div><!-- / page -->

    <footer>
      
    </footer>
  </div><!-- / app -->
</template>

<script>
export default {
  name: 'app',
}
</script>
<!-- styling for the component -->
<style>
body {
  margin: 0;
  /*
  background: -webkit-linear-gradient(180deg, rgb(246, 114, 128), rgb(53, 92, 125));
  background: linear-gradient(180deg, rgb(246, 114, 128), rgb(53, 92, 125));
  */
}

#app {
  font-family: 'Montserrat', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
}

header {
  display: grid;
  grid-template-columns: 1fr 4fr;
  grid-column-gap: 1em;
  padding: 0 30px;
}

header .logo {
  
}

nav {
  text-align: right;
}
</style>
