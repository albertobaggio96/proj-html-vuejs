<script>
import NavBar from './header-components/NavBar.vue';
import JumboApp from './header-components/JumboApp.vue';

export default {
  components:{
    NavBar,
    JumboApp,
  }
}
</script>

<template>
  <header class="bg-black text-white pt-3 px-3 fw-bold">
    <NavBar/>
    <section id="jumbo" class="row">
      <JumboApp />
    </section>
  </header>
</template>

<style lang="scss">
  header{
    background-image: url(../assets/img/bg-header.png);
    font-family: 'Oswald', sans-serif;
  }
</style>