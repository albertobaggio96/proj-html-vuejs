<script>
import NewspapersReviews from './main-components/NewspapersReviews.vue'
import PizzaSpecials from './main-components/PizzaSpecials.vue';
import DontJudgePizza from './main-components/DontJudgePizza.vue';
import BookingApp from './main-components/BookingApp.vue'

export default {
  components: {
    NewspapersReviews,
    PizzaSpecials,
    DontJudgePizza,
    BookingApp
  },
  data() {
    return {
      advertisingImagesList: ["New Place", "Mangia una buona pizza", "Yum Elvis", "La pizza più grande"],
      advertisingImagePath: "h3-img-",
      teamPath: "h1-team-",
      teamNames: [{
        name: "Paolo Rossi",
        path: "1a-700x700",
        role: "Pizzaiolo"
      },
      {
        name: "Francesca Zaia",
        path: "2a",
        role: "Waiter"
      },
      {
        name: "Frank Bailey",
        path: "4a",
        role: "Kitchen Porter"
      },
      {
        name: "Gioia Bellavia",
        path: "3a",
        role: "Manager"
      },
      ],
      clientsPath: "h1-clients-img-",
      clientList: [{
        name: "Cowboy",
        path: 4,
      },
      {
        name: "Gordon",
        path: 3,
      },
      {
        name: "Big Cheese",
        path: 1,
      },
      {
        name: "Bludoos Bar",
        path: 2,
      },
      {
        name: "Vegan",
        path: 5,
      }
      ],
      prodactsPath: "h3-product-img-",
      prodactsList: [{
        name: "Bismark",
        path: "1a-100x100",
        originalPrice: "$35.00",
        price: "$30.00"
      },
      {
        name: "Fior Di Zucca",
        path: "2a-150x150",
        originalPrice: "",
        price: "$7.00 -$50.00"
      },
      {
        name: "Valdostana",
        path: "3a-150x150",
        originalPrice: "",
        price: "$55.00"
      },
      {
        name: "Pizza Tartufata",
        path: "4a-150x150",
        originalPrice: "",
        price: "$45.00"
      },
      {
        name: "Francescana",
        path: "5a-150x150",
        originalPrice: "",
        price: "$25.00"
      },
      {
        name: "Campagnola",
        path: "6a-100x100",
        originalPrice: "",
        price: "$50.00 - 95.00$"
      },
      ],
    }
  },
  methods: {
    getImgPath(imgPathstart, imgPathEnd = "", fileFormat) {
      return new URL(`../assets/img/${imgPathstart}${imgPathEnd}.${fileFormat}`, import.meta.url).href;
    },
  }
}
</script>

<template>
  <main>
    
    <section id="advertising-images" class="row">
      <article class="col-lg-3 g-1" v-for="(alt, index) in advertisingImagesList">
        <img class="img-fluid" :src="getImgPath(advertisingImagePath, index + 1, 'jpg')" :alt="alt">
      </article>
    </section>

    <section id="newspapers-reviews" class="row">
      <NewspapersReviews />
    </section>

    <section id="pizza-specials" class="row">
      <PizzaSpecials />
    </section>

    <section id="dont-judje-pizza" class="row">
      <DontJudgePizza />
    </section>

    <section id="team-presentation" class="row">
      <article class="col-lg-3 px-0" v-for="(person) in teamNames">
        <img class="img-fluid" :src="getImgPath(teamPath, person.path, 'jpg')" :alt="person.name">
      </article>
    </section>

    <section id="clients-logo">
      <div class="container px-5">
        <div class="row p-5">
          <figure class="col " v-for="(client, index) in clientList">
            <img class="img-fluid" :src="getImgPath(clientsPath, client.path, 'png')" :alt="client">
          </figure>
        </div>
      </div>
    </section>

    <section id="best-pizza">
      <article class="text-center">
        <div>CHOOSE YOUR FLAVOR</div>
        <h2>THE BEST PIZZA MENU IN TOWN</h2>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Velit neque error soluta officia cumque dolores corrupti quidem totam illum.</p>
      </article>
      <ul class="d-flex p-0 flex-nowrap justify-content-between">
        <li class="list-group-item" v-for="pizza in prodactsList">
          <figure>
            <img :src="getImgPath(prodactsPath, pizza.path, 'png')" :alt="pizza.name">
          </figure>
          <h3>{{ pizza.name.toUpperCase() }}</h3>
          <div>{{ pizza.price }}</div>
        </li>
      </ul>
    </section>

    <section id="delish-pizza" class="row">
      <PizzaSpecials/>
    </section>

    <section id="booking">
      <BookingApp/>
    </section>
  </main>
</template>

<style lang="scss" scoped>
    section#best-pizza{
      ul{
        overflow-x: auto;
        li{
          padding: 0 50px;
        }
        img{
          width: 200px;
        }
      
      }
    }
</style>