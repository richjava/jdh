<template>
  <header>
      <div class="logo">
        A small amount of text
      </div><!-- / logo -->
      <div class="menu">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Consequatur sed natus beatae qui perspiciatis quis, aperiam quisquam, odio accusamus sit minima molestias consectetur porro ab deserunt, asperiores placeat maiores illo.
      </div><!-- / menu -->
  </header>
</template>

<script>
export default {
  name: 'menu'
}
</script>

<style scoped>
    header {
        display: grid;
    }

    header .logo {
        background: blue
    }

    header .menu {
        background: red
    }
</style>
