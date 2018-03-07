<template>
  <div class="joel">
    <a href="#" target="_blank">
      <div class="gradient-mask">
        <div class="project-link">
          <h2>{{ name }}</h2>
          <p>{{ project }}</p>
        </div><!-- / project link -->
      </div><!-- / gradient mask -->
    </a>
  </div>
</template>

<script>
export default {
  name: 'joel',
  data () {
    return {
      name: 'Joel Withers',
      project: 'The Joel Withers Project'
    }
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
  color: #fff;
  text-decoration: none;
}


.joel {
  position: relative;
  height: 100vh;
  background-image: url(../../assets/homepage_images/Joel-sized.jpg);
}

.gradient-mask {
  height: 100%;
  background: -webkit-linear-gradient(90deg, rgba(255, 255, 255, 0), rgba(127, 38, 31, 0.5));
  background: linear-gradient(90deg, rgba(255, 255, 255, 0), rgba(127, 38, 31, 0.5));
}

.gradient-mask:after {
  position: absolute;
  content: '';
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  transition: opacity 0.5s ease;
  z-index: 3;
  background: -webkit-linear-gradient(90deg, rgba(127, 38, 31, 0.8), rgba(127, 38, 31, 0.8));
  background: linear-gradient(90deg, rgba(127, 38, 31, 0.8), rgba(127, 38, 31, 0.8));
  opacity: 0;
}

.gradient-mask:hover:after {
  opacity: 1;
}

.joel .project-link {
  position: absolute;
  bottom: 30px;
  left: 30px;
  z-index: 5;
  -webkit-transition:all 0.5s ease;
       -moz-transition:all 0.5s ease;
        -ms-transition:all 0.5s ease;
         -o-transition:all 0.5s ease;
            transition:all 0.5s ease;
}

.gradient-mask:hover .project-link {
  bottom: 50%;
}

.project-link h2 {
  text-transform: uppercase;
  font-size: 34px;
  margin: 0px;
}

.project-link p {
  text-transform: lowercase;
}
</style>
