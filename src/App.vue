<template>
  <div id="app">
    <!-- navbar -->
    <header>
      <NavbarHeader />
    </header>

    <!-- jumbotron -->
    <section>
      
    </section>

    <!-- content -->
    <main>
      <!-- info team -->
      <!-- countdown -->
      <!-- team members -->
      <!-- program company-->
      <!-- location and map -->
      <!-- news -->
      <!-- tickets -->
      <!-- media -->
      <!-- sponsor company -->
    </main>
      
    <!-- footer -->
    <footer>

    </footer>
  </div>
</template>

<script>
import NavbarHeader from './components/NavbarHeader.vue';


export default {
  name: 'App',
  components: {
    NavbarHeader
}
}
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0 !important;
  padding: 0;
}

@import url('https://fonts.googleapis.com/css2?family=Source+Sans+Pro:wght@200;300;400;600;700;900&display=swap');

#app {
  font-family: Source Sans Pro, Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
