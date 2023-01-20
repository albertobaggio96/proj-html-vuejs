<script>
export default {
  
}
</script>

<template>
  <div class="d-flex justify-content-center align-items-center">
    <div class="input-group">
      <input type="text" placeholder="1 Person" id="person" class="border border-dark py-3 ps-2">
      <span class="input-group-text bg-white border border-start-0 border-dark rounded-0 p-0"><font-awesome-icon icon="fa-regular fa-user" class="fa"/></span>
    </div>
    <span class="px-4 text-white fw-bold">FOR</span>
    
    <div class="input-group">
      <input type="data" placeholder="01/18/2023" class="border border-dark py-3 ps-2">
      <span class="input-group-text bg-white border border-start-0 border-dark rounded-0 p-0"><font-awesome-icon icon="fa-regular fa-calendar" class="fa"/></span>
    </div>
    <span class="px-4 text-white fw-bold">AT</span>
    <div class="input-group">
      <input type="text" placeholder="7:00 pm" class="border border-dark py-3 ps-2">
      <span class="input-group-text bg-white border border-start-0 border-dark rounded-0 p-0"><font-awesome-icon icon="fa-regular fa-clock" class="fa"/></span>
    </div>
    <button class="ms-5 py-3 text-white">BOOK A TABLE</button>
  </div>
</template>

<style lang="scss" scoped>
  @use "../../style/partials/variables" as *;

  div.input-group,
  button{
    width: 222px;
  }
  button{
    background-color: $orange-button;
  }  
  .fa{
    width: 38px;
    color: $gold;
  }


</style>