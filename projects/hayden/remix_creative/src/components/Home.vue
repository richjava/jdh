<template>
  <div class="home">
    <div class="banner"> 
      <img src="../assets/home-banner.png" alt="">
      <h1>This is Remix Creative</h1>
    </div><!-- / banner -->

    <div class="projects">
      <ul>
        <li></li>
      </ul>
    </div><!-- / projects -->
  </div><!-- / home -->
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods: {
    getDesigners: function() {
        this.$http.jsonp('http://behance.net/v2/users/haydenwrat86b8/following?api_key=wmkhz92FaRjQt4LZzE0L3akK6CXqQOMB')
        .then(response => {
            this.users = response.body.following;
            console.log(response.body.following)
        });
    }
  },
  created: function() {
    this.getDesigners();
    console.log();
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
