<script>
import NewspapersReviews from './main-components/NewspapersReviews.vue'
import PizzaSpecials from './main-components/PizzaSpecials.vue';
import DontJudgePizza from './main-components/DontJudgePizza.vue';
import DelishPizza from './main-components/DelishPizza.vue';
import BookingApp from './main-components/BookingApp.vue'

export default {
  components: {
    NewspapersReviews,
    PizzaSpecials,
    DontJudgePizza,
    DelishPizza,
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
      <article class="col-lg-3 g-1 position-relative" v-for="(alt, index) in advertisingImagesList">
        <img class="img-fluid" :src="getImgPath(advertisingImagePath, index + 1, 'jpg')" :alt="alt">
        <div class="mouse-hover position-absolute top-0 w-100 h-100 d-flex justify-content-center align-items-center">
          <font-awesome-icon icon="fa-regular fa-eye" class="fs-3 fa-hover p-3 rounded-circle"/>
        </div>
      </article>
    </section>

    <section id="newspapers-reviews" class="row px-3">
      <NewspapersReviews />
    </section>

    <section id="pizza-specials" class="row">
      <PizzaSpecials />
    </section>

    <section id="dont-judge-pizza" class="row">
      <DontJudgePizza />
    </section>

    <section id="team-presentation" class="row">
      <article class="col-lg-3 px-0 position-relative" v-for="(person) in teamNames">
        <img class="img-fluid" :src="getImgPath(teamPath, person.path, 'jpg')" :alt="person.name">
        <div class="mouse-hover position-absolute top-0 w-100 h-100 d-flex justify-content-center align-items-center">
          <div class="fs-3 fa-hover p-3 d-flex justify-content-center align-items-center text-center text-white person">
            <article>
              <h2 class="fw-bold fa-hover">{{ person.name.toUpperCase()}}</h2>
              <div class="fa-hover fs-5">{{ person.role }}</div>
              <div class="fa-hover">
                <font-awesome-icon icon="fa-brands fa-instagram" class="px-2 fs-5"/>
                <font-awesome-icon icon="fa-brands fa-twitter" class="px-2 fs-5"/>
                <font-awesome-icon icon="fa-brands fa-facebook-f" class="px-2 fs-5"/>
              </div>
            </article>

          </div> 
        </div>
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
      <article class="text-center mx-auto pb-5">
        <div class="orange-text fw-bold">CHOOSE YOUR FLAVOR</div>
        <h2 class="fw-bolder mb-3">THE BEST PIZZA MENU IN TOWN</h2>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Velit neque error soluta officia cumque dolores
          corrupti quidem totam illum.</p>
      </article>
      <ul class="d-flex p-0 flex-nowrap justify-content-between text-center">
        <li class="list-group-item" v-for="pizza in prodactsList">
          <figure>
            <img :src="getImgPath(prodactsPath, pizza.path, 'png')" :alt="pizza.name">
          </figure>
          <h3 class="fw-bold">{{ pizza.name.toUpperCase() }}</h3>
          <div class="fw-bold orange-text">{{ pizza.price }}</div>
        </li>
      </ul>
    </section>

    <section id="delish-pizza" class="row">
      <DelishPizza />
    </section>

    <section id="booking" class="my-2">
      <BookingApp />
    </section>

  </main>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables.scss" as *;
  article.position-relative{
    div.mouse-hover,
    .fa-hover{
          opacity: 0;
          transition: .5s;
    }
    .person{
      width: 90%;
      height: 90%;
    }

    &:hover{
      div.mouse-hover{
          background-color: white;
          opacity: 1;
      }
      .fa-hover{
        opacity: 1;
        background-color: $orange-button;
      }
    }
  }


section#newspapers-reviews {
  background-image: url(../assets/img/h3-testimonials-bckgrnd.jpg);
  background-size: cover;
  background-position: center;
}

section#clients-logo {
  background-color: $bg-super-light-gary;
}

section#best-pizza {

  article {
    width: 600px;
    padding-top: 100px;
    p {
      color: $gray-special;
    }
  }
  ul {
    overflow-x: auto;
    margin-bottom: 100px;
      li {
      padding: 0 50px;
      img {
        width: 200px;
      }
      h3{
        font-size: 1rem;
        color: $gold-text;
      }
    }
  }
  .orange-text {
    color: $orange-text;
    font-size: .8rem;
  }
  
}

section#booking{
  padding: 80px;
  background-image: url(../assets/img/h3-background-img-3.jpg);
  background-size: cover;
}

</style>