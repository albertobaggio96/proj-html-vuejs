<script>

export default {
  
}
</script>

<template>
  <div class="col-lg-12 px-0 text-center py-3 position-relative carosel-container">
    <button class="rounded-circle pre position-absolute">PREV</button>
    <img class="position-absolute top-50 start-50 translate-middle" src="../../assets/img/h3-rev-img-1.png" alt="">
    <img class="position-absolute top-50 start-50 translate-middle" src="../../assets/img/h3-rev-img-2.png" alt="Urban Taste">
    <button class="rounded-circle nt position-absolute">NEXT</button>
  </div>
</template>

<style lang="scss" scoped>

@use "../../style/partials/variables" as *;
  .carosel-container{
    height: 560px;
    button{
      width: 95px;
      height: 95px;
      padding-bottom: 50px;
      top: calc(50% - 40px);
      color: $orange-button;
    }
    button.pre{
      transform: rotate(90deg);
      left: -60px;
    }
    button.nt{
      transform: rotate(270deg);
      right: -60px;
    }
  }
</style>