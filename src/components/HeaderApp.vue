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
  <header class="bg-black text-white p-3">
    <NavBar/>
    <section id="jumbo" class="row">
      <JumboApp />
    </section>
  </header>
</template>

<style lang="scss">
  
</style>