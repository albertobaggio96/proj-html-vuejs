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

  button{
    border: none;
  }
</style>
