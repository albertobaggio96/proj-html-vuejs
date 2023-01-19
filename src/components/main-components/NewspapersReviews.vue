<script>

export default {
  
}
</script>

<template>
  <div class="col-lg-12 d-flex justify-content-center align-items-center px-0 text-center py-3 position-relative carosel-container">
    <button class="rounded-circle pre position-absolute">PREV</button>
    <article class="container">
      <font-awesome-icon icon="fa-solid fa-quote-left" class="gold quote-left" />
      <p class="fs-3 mb-2 fw-bold">"FORGHET THE TRENDY PIZZA SHOPS, THIS HIDDEN SPOT MAKES THE BEST NEW YOEK-STYLE PIZZA SLICE IN NAPLES"</p>
      <div class="mb-3 newspaper">WHASHINGTON POST 2018</div>
      <font-awesome-icon icon="fa-solid fa-circle" class="gold pe-2 dot" /><font-awesome-icon icon="fa-solid fa-circle" class="l-gray pe-2 dot" /><font-awesome-icon icon="fa-solid fa-circle" class="l-gray dot"/>
    </article>
    <button class="rounded-circle nt position-absolute">NEXT</button>
  </div>
</template>

<style lang="scss" scoped>

@use "../../style/partials/variables" as *;
  .carosel-container{
    height: 485px;

    article{
      padding: 0 220px;
      .gold{
        color: $gold;
      }
  
      .l-gray{
        color: $light-gray;
      }
      .quote-left{
        font-size: 100px;
      }

      .newspaper{
        color: $orange-text;
      }

      .dot{
        font-size: .6rem;
      }
    }
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