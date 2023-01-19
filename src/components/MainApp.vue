<script>
import JumboApp from './main-components/JumboApp.vue';
import NewspapersReviews from './main-components/NewspapersReviews.vue'
import PizzaSpecials from './main-components/PizzaSpecials.vue';
import DontJudgePizza from './main-components/DontJudgePizza.vue'

export default {
  components: {
    JumboApp,
    NewspapersReviews,
    PizzaSpecials,
    DontJudgePizza,
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
      clientList: ["Cowboy", "Gordon", "Big Cheese", "Bludoos Bar", "Vegan"]
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
    <section id="jumbo" class="row">
      <JumboApp />
    </section>

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
            <img class="img-fluid" :src="getImgPath(clientsPath, index + 1, 'png')" :alt="client">
          </figure>
        </div>
      </div>
    </section>
  </main>
</template>

<style lang="scss">

</style>