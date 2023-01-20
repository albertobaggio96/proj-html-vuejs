<script>
export default {
  
}
</script>

<template>
  <section>
    <figure>
      <img src="../assets/svg/svg-7.svg" alt="rolated" class="rolated">
    </figure>
    <figure>
      <img src="../assets/svg/svg-9.svg" alt="shop" class="shop bg-white"> 
    </figure>
    <figure>
      <img src="../assets/svg/svg-4.svg" alt="slice" class="slice rounded-circle position-relative">
    </figure>
  
  </section>
</template>

<style lang="scss" scoped>
  @use "../style/partials/variables.scss" as *;

  section{
    position: fixed;
    right: 0;
    top: 65%;
    z-index: 1;
    .rolated{
      background-color: $rolated;
      width: 40px;
      padding: 7px;
    }
    .shop{
      width: 40px;
      padding: 7px;
      margin-bottom: 80px;
    }
    .slice{
      width: 40px;
      height: 40px;
      padding: 7px;
      right:  15px;
      background-color: $bg-super-light-gary;
    }

    
    
  }
</style>