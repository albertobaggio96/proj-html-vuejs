<script>
  import HeaderApp from './components/HeaderApp.vue';
  import MainApp from './components/MainApp.vue';
  import FooterApp from './components/FooterApp.vue';

  export default{
    components : {
      HeaderApp,
      MainApp,
      FooterApp
    }
  }
</script>

<template>
  <HeaderApp/>

  <MainApp/>

  <FooterApp/>
</template>

<style lang="scss" >
  @use "./style/partials/variables.scss" as *;
  @use "./style/general.scss" as *;
  @use "../node_modules/bootstrap/scss/bootstrap.scss" as *;

  body{
    overflow-x: hidden;
    font-family: 'Roboto Condensed', sans-serif;
  }
  button{
    border: none;
  }
</style>
