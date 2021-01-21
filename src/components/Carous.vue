<template>
    <div class="carousel-container ">
        <div>
            <VueSlickCarousel v-bind="settings">
               <div><h3>1</h3></div>
               <div>2</div>
               <div>3</div>
               <div>4</div>
               <div>5</div>
            </VueSlickCarousel>
        </div>
    </div>
</template>
<script>
  import VueSlickCarousel from 'vue-slick-carousel'
  import 'vue-slick-carousel/dist/vue-slick-carousel.css'
  // optional style for arrows & dots
  import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
export default {
    name: 'Carous',
    data: function(){
        return{
            settings:{
                "dots": true,
                "focusOnSelect": true,
                "infinite": true,
                "speed": 500,
                "slidesToShow": 3,
                "slidesToScroll": 3,
                "touchThreshold": 5
            }
        }
    },
    components:{
        VueSlickCarousel
    }
}
</script>
<style lang="scss" scoped>
  .carousel-container{
  }
</style>