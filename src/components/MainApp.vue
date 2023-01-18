<script>
import JumboApp from './main-components/JumboApp.vue';
import NewspapersReviews from './main-components/NewspapersReviews.vue'

export default {
  components:{
    JumboApp,
    NewspapersReviews,
  },
  data(){
    return{
      advertisingImages: ["New Place", "Mangia una buona pizza", "Yum Elvis", "La pizza più grande"]
    }
  },
  methods:{
    getImgPath(imgPath){
      return new URL(`../assets/img/h3-img-${imgPath + 1}.jpg`, import.meta.url).href;
    },
  }
}
</script>

<template>
  <main>
    <section id="jumbo" class="row">
      <JumboApp/>
    </section>

    <section id="advertising-images" class="row">
      <div class="col-lg-3 g-1" v-for="(alt, index) in advertisingImages">
        <img class="img-fluid" :src="getImgPath(index)" :alt="alt">
      </div>
    </section>

    <section id="newspapers-reviews" class="row">
      <NewspapersReviews/>
    </section>
  </main>
</template>

<style lang="scss">
  
</style>