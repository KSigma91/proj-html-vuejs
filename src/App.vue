<template>
  <div id="app">
    <!-- navbar -->
    <header>
      <NavbarHeader />
    </header>

    <!-- content -->
    <main>
        <MainContent />
    </main>
      
    <!-- footer -->
    <footer>
      <MyFooter />
    </footer>
  </div>
</template>

<script>
import NavbarHeader from './components/NavbarHeader.vue';
import MainContent from './components/MainContent.vue';
import MyFooter from './components/MyFooter.vue';

export default {
  name: 'App',
  components: {
    NavbarHeader,
    MainContent,
    MyFooter
}
}
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0 !important;
  padding: 0 !important;
}

/* @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100;200;300;400;500;600;700;800&display=swap'); */
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap');

#app {
  font-family: 'Poppins', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
