<template>
  <div id="nav">
    <NavBar />
  </div>
  <router-view/>
</template>

<script>
import NavBar from '@/components/NavBar.vue'

export default {
  components: {
    NavBar
  }
}
</script>
<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@200;300;400;500;600;700&display=swap');

#app {
  font-family: 'Montserrat', sans-serif, Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: #f1f1f1;
}
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
</style>
