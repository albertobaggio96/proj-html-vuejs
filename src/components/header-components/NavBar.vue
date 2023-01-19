<script>
export default {
  
}
</script>

<template>
  <nav class="container">
    <div class="row justify-content-between align-items-center">
      <div class="col">
        <button class="col ms-4 px-4 py-3 mb-3">ORDER ONLINE</button>
      </div>
      <ul class="d-flex align-items-center justify-content-center j col-6">
        <li class="list-group-item px-3 d-flex"><img class="icon-img me-1" src="../../assets/svg/svg-0.svg" alt="moustache">HOME</li>
        <li class="list-group-item px-3">PAGES</li>
        <li class="list-group-item px-3">MENU</li>
        <li class="list-group-item px-3"><img class="don-peppe-logo" src="../../assets/img/h5-logo-divided-header.png" alt="Don Peppe logo"></li>
        <li class="list-group-item px-3">EVENT</li>
        <li class="list-group-item px-3">BLOG</li>
        <li class="list-group-item px-3">LANDING</li>
      </ul>
      <ul class="col d-flex justify-content-end me-4">
        <li class="list-group-item px-3"><img class="icon-img me-1" src="../../assets/svg/svg-1.svg"> CART</li>
        <li class="list-group-item px-3"><font-awesome-icon icon="fa-solid fa-magnifying-glass" /> SEARCH</li>
      </ul>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
  @use "../../style/partials/variables" as *;

  button{
    background-color: $orange-button;
    color: $white;
    font-size: .8rem;
  }
  li{
    font-size: .8rem;
    img.icon-img{
      filter: invert(100%);
      width: 15PX;
      
    }
    img.don-peppe-logo{
      width: 170px;
    }
  }
  
</style>