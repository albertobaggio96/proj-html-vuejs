<script>
export default {
  data(){
    return{
      specialMenu:[
      {
          price: "$10",
          name: "Combo Piccolo",
          descrition: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia deserunt unde alias?"
        },
        {
          price: "$20",
          name: "Combo Mezzo",
          descrition: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia deserunt unde alias?"
        },
        {
          price: "$10",
          name: "Combo Grande",
          descrition: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia deserunt unde alias?"
        },
        
      ]
    }
  }
}
</script>

<template>
  <figure class="col-lg-6  position-relative">
    <img class="img-fluid" src="../../assets/img/h1-img-4.jpg" alt="spacial pizzas">
    <img class="position-absolute pizza-specials-logo" src="../../assets/img/h1-img-7n.png" alt="special pizza">
  </figure>
  <article class="col-lg-6 d-flex justify-content-center align-items-center ">
    <div class="spercials-menu">
      <h2>SPECIALS*</h2>
      <P> Lorem ipsum dolor sit amet consectetur adipisicing elit. Explicabo, nisi.</P>
      <ul class="p-0">
        <li class="list-group-item d-flex" v-for="pizza in specialMenu">
          <div class="price fw-bold pe-2">{{pizza.price}}</div>
          <div>
            <div class="name-pizza fw-bold mb-1">{{ pizza.name.toUpperCase() }}</div>
            <p>{{ pizza.descrition }}</p>
          </div>
        </li>
        
      </ul>
    </div>
  </article>
</template>

<style lang="scss" scoped>
@use "../../style/partials/variables" as *;

p{
  color:$gray-special;
}

.pizza-specials-logo{
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.spercials-menu{
  width: 400px;
}

.price{
  color: $price-special-menu;
}
  


</style>