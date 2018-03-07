<template>
  <div class="intro">
    <h1>JDH</h1>
    <div class="catchphrase">
      <p>{{ msg }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'intro',
  data () {
    return {
      msg: 'A group of friends making no difference.'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: bold;
}

h1 {
  font-size: 60px;
}

p {
  font-size: 40px;
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

.intro {
  padding: 30px;
}
</style>
