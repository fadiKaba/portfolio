<template>
    <div class="carousel-container ">
        <carousel>
            <slide>
                Slide 1 Content
            </slide>
            <slide>
                Slide 2 Content
            </slide>
            <slide>
                Slide 2 Content
            </slide>
        </carousel>
    </div>
</template>
<script>
import { Carousel, Slide } from 'vue-carousel';
export default {
    name: 'Carous',
    components:{
        Carousel, Slide
    }
}
</script>
<style lang="scss" scoped>
  .carousel-container{
  }
</style>