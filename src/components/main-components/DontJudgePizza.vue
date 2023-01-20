<script>
export default {
  
}
</script>

<template>
  <div class="col-lg-12 position-relative">
    <div class="special-bg up"></div>
    <div class="special-bg middle"></div>
    <div class="special-bg down"></div>
    <h1 class="position-absolute dont-judge text-white fw-bolder">
      GO AHEAD AND <br>
      BIILD YOUR <br>
      OWN PIZZA <br>
      WE WON'T <br>
      JUDGE!
    </h1>
  </div>
</template>

<style lang="scss">
  .special-bg{
    background-image: url(../../assets/img/h3-background-img.jpg);
    background-size: 90%;
    background-position-x: center;
  }
  .up{
    height: 100px;
    background-position-y: bottom;
  }
  .middle{
    height: 250px;
  }
  .down{
    height: 100px;
    background-position-y: 65%;
  }

  .dont-judge{
    top: 50%;
    transform: translate(0, -50%);
    left: 20%;
    font-size: 3rem
  }

</style>