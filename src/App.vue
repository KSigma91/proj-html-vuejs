<template>
  <div id="app">
    <!-- navbar -->
    <header>
      <NavbarHeader />
    </header>

    <!-- content -->
    <main>
      <section>
        <!-- jumbotron -->
        <MainContent />
      </section>
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
import MainContent from './components/MainContent.vue';

export default {
  name: 'App',
  components: {
    NavbarHeader,
    MainContent
}
}
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0 !important;
  padding: 0 !important;
}

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100;200;300;400;500;600;700;800&display=swap');

#app {
  font-family: Montserrat, Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
