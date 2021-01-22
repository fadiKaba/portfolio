<template>
    <div class="carousel-container mt-2 mt-md-5 border-bottom" id="car">
        <div class="py-2 py-md-5">
            <VueSlickCarousel v-bind="settings" class="caro">
               <div class="text-center px-2 px-md-5">
                   <img class="mx-auto mb-2 mb-md-4" src="../assets/iconic/design.png" alt="design" width="60px">
                   <h3 class="mb-2 mb-md-4 blue-title">Web design </h3>
                   <p class="">Responsive design | Programming dynamic websites | Development of functions to improve the user experience (UX)</p>
               </div>
               <div class="text-center px-2 px-md-5">
                   <img class="mx-auto mb-2 mb-md-4" src="../assets/iconic/front.png" alt="design" width="60px">
                   <h3 class="mb-2 mb-md-4 blue-title">FRONTEND WEB DEVELOPMENT </h3>
                   <p class="">Test and improve the design of the website using web technologies | Integration of functions and features in the websites</p>
               </div>
               <div class="text-center px-2 px-md-5">
                   <img class="mx-auto mb-2 mb-md-4" src="../assets/iconic/back.png" alt="design" width="60px">
                   <h3 class="mb-2 mb-md-4 blue-title">BACKEND WEB DEVELOPMENT</h3>
                   <p class="">create and support high-level back-end projects for one project or multiple projects</p>
               </div>
               <div class="text-center px-2 px-md-5">
                   <img class="mx-auto mb-2 mb-md-4" src="../assets/iconic/innovation.png" alt="design" width="60px">
                   <h3 class="mb-2 mb-md-4 blue-title">Innovation</h3>
                   <p class="">create and support high-level back-end projects for one project or multiple projects</p>
               </div>
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
               // "dots": true,
                "infinite": true,
                "speed": 800,
                "slidesToShow": 3,
                "slidesToScroll": 1,
                "prevArrow": document.querySelector('.prev'),
                "nextArrow": document.querySelector('.next'),
                "initialSlide": 0,
               "autoplay": true,
               "autoplaySpeed": 2000,
               "pauseOnDotsHover": true,
               "pauseOnFocus": true,
               "pauseOnHover": true,
                "responsive": [
                    {
                    "breakpoint": 1024,
                        "settings": {
                            "slidesToShow": 3,
                            "slidesToScroll": 3,
                            "infinite": true,
                            "dots": true
                        }
                    },
                    {
                    "breakpoint": 600,
                        "settings": {
                            "slidesToShow": 2,
                            "slidesToScroll": 2,
                            "initialSlide": 2
                        }
                    },
                    {
                    "breakpoint": 480,
                        "settings": {
                            "slidesToShow": 1,
                            "slidesToScroll": 1
                        }
                    }
                ]
            }
        }
    },
    components:{
        VueSlickCarousel
    }
}
</script>
<style lang="scss" scoped>
  $color1: #488CEA;
  .carousel-container{
      .caro{
      }
  }
</style>