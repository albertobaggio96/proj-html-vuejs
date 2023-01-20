<script>
export default {
  data(){
    return{
      events:[
      {
        day: "02",
        month: "November",
        title: "Traditional napolitan pies in kyoto pizza mercato",
        where: "204 E, Piazzetta Tommaso"
      },
      {
        day: "03",
        month: "November",
        title: "Terarazza patio dining space opening this weekend",
        where: "204 E, Piazzetta Tommaso"
      },
      {
        day: "05",
        month: "November",
        title: "Sienna private dining room with Stéphane Brunn",
        where: "204 E, Piazzetta Tommaso"
      },
      ]
    }
  }
}
</script>

<template>
  <div class="col-lg-6 d-flex justify-content-center align-items-center bg-stars text-white">
    <div class="delish-menu">
      <div class="red-orange over-title">MADE WITH LOVE</div>
      <h2>DELISH PIZZA DEALS</h2>
      <ul class="px-0">
        <li v-for="(event, index) in events" class="d-flex align-items-start pt-4 list-group-item" :class="index < events.length - 1 ? 'border-dotted pb-4' : ''">
          <div class="pe-2">
            <div class="red-orange fw-bolder fs-1 lh-1">{{ event.day }}</div>
            <div class="fw-bold">{{ event.month.substring(0,3).toUpperCase() }}</div>
          </div>
          <div>
            <h3 class="fs-5 fw-bold mb-0">{{ event.title.toUpperCase() }}</h3>
            <div class="red-orange">{{ event.where }}</div>
          </div>
        </li>
      </ul>
    </div>
  </div>
  <div class="col-lg-6 ps-0">
    <img class="img-fluid" src="../../assets/img/h3-img-5a.jpg" alt="super-pizza">
  </div>
</template>

<style lang="scss">
@use "../../style/partials/variables" as *;

  .bg-stars{
    background-image: url(../../assets/img/bg-header.png);
    padding: 80px;
    margin-bottom: 80px;
  }
  .delish-menu{
    width: 400px;

    .over-title{
      font-size: .7rem;
    }
    .red-orange{
      color: $red-orange;
    }
    .border-dotted{
      border-bottom: 3px dotted $gold;
    }
  }
</style>