<template>
    <div class="main-container">
        <div class="cover"> 
            <Navbar></Navbar>
            <img class="mx-auto" width="10px" src="../assets/svg_folder/wave.svg" alt="wave"> 
            <main class="container">
                <div class="title mt-5 py-5">
                    <p class="white para1 ">Hello, My Name is</p>
                    <h1 class="white">FADI KABA</h1>
                    <p class="white para2">Backend and frontend web developer</p>
                    <a href="#about" class="btn btn-light">Contact me</a>
                </div>
                     <Carous></Carous>  
                     <About></About>
                     <Skills></Skills>
                     <Experience></Experience>  
            </main> 
            <Footer></Footer>        
        </div>
    </div>
</template>
<script>

import Navbar from './Navbar';
import Carous from './Carous';
import About from './About';
import Skills from './Skills';
import Experience from './Experience';
import Footer from './Footer';

export default {
    name:'Main',
    data: function(){
        return{
            
        }
    },
    components:{
        Navbar, Carous, About, Skills, Experience, Footer
    },
    mounted: function(){
    },
    methods:{
      
    },
    computed: {

    }
}
</script>
<style scoped lang="scss">
   $color1:#488CEA;
   $color2:#89B7F7;
   $color3: rgb(75, 194, 226);
   .main-container{
       text-align:center;
       font-family: 'Open Sans', sans-serif;;
       .cover{
          background-color: $color1; 
          height: 100vh;
          position:relative;
          img{
              position:absolute;
              bottom:0;
              left:0;
              width: 98.9vw;
          }
       } 
       .white{
           color:#fff;
       }   
       main{
          .title{
              height: 100vh;
              .para1{
                  font-weight:bold;
              }
              h1{
                  font-weight: bold;
              }
              a{
                  border:none;
                  border-radius: 25px;
                  background-color: $color3;
                  color:#fff;
                  position: relative;
                  &:hover{
                      background-color: $color2;
                  }
              }
          }
       }
   }
    button.slick-prev:before, button.slick-next:before {
      background-color: red !important;
}

</style>