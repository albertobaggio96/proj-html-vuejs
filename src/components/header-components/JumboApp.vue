<script>

export default {
  data(){
    return{
      index: 0,
      fileFormat: "png",
      JumboImgList:[
        {
          pathKeyWord: "h3-rev-img-1",
          pathKeyPizza: "h3-rev-img-2",
          active : true
        },
        {
          pathKeyWord: "h3-rev-img-3",
          pathKeyPizza: "h3-rev-img-4",
          active : false
        },
        {
          pathKeyWord: "h3-rev-img-5",
          pathKeyPizza: "h3-rev-img-6",
          active : false
        },
      ],
      timer: "",
    }
  },
  methods:{
    getImgPath(imgPathstart, fileFormat) {
      return new URL(`../../assets/img/${imgPathstart}.${fileFormat}`, import.meta.url).href;
    },

    getNextCarosel(array){
      array[this.index].active = false
      this.index ++
      if(this.index > array.length -1){
        this.index = 0
      } 
      return array[this.index].active = true
    },

    getPrevCarosel(array){
      array[this.index].active = false
      this.index--
      if(this.index === 0){
        this.index = array.length -1
      }
      return array[this.index].active = true
    },
    getStartTimer(){
      this.timer = setInterval(this.getNextCarosel, 4000, this.JumboImgList);
    }
  },
  created(){
    this.getStartTimer()
  }
}
</script>

<template>
  <div class="col-lg-12 px-0 text-center py-3 position-relative carosel-container overflow-hidden">
    <button class="rounded-circle pre position-absolute" @click="getPrevCarosel(JumboImgList)">PREV</button>
      <div v-for="img in JumboImgList">
        <img :src=" getImgPath(img.pathKeyWord, fileFormat)" alt="" :class="img.active ? 'active' : 'd-none'"  class="position-absolute top-50 start-50 translate-middle key-word w-75">
        <img :src="getImgPath(img.pathKeyPizza, fileFormat)" alt="Urban Taste"  :class="img.active ? 'active' : 'd-none'" class="position-absolute top-50 start-50 translate-middle pizza">
      </div>
    <button class="rounded-circle nt position-absolute" @click="getNextCarosel(JumboImgList)">NEXT</button>
  </div>
</template>

<style lang="scss" scoped>

@use "../../style/partials/variables" as *;
  .carosel-container{
    height: 560px;
    .key-word.active{
      animation-name: key-word;
      animation-duration: .7s;
      animation-timing-function: linear;
      animation-iteration-count: 1;
    }
    .pizza.active{
      animation-name: pizza;
      animation-duration: .7s;
      animation-timing-function: linear;
      animation-iteration-count: 1;
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

  @keyframes key-word {
    0%{
      padding: 200px;
      opacity: .5;
    }
    50%{
      padding: 0px;
      opacity: 1;
    }
    
    100%{
      padding: 0;
      opacity: 1;
    }
  }
  @keyframes pizza {
    0%{
      translate: 0 -100px;
      opacity: 0;
    }
    50%{
      translate: 0 -100px;
      opacity: 0;
    }
    
    100%{
      translate: 0px;
    }
  }
</style>