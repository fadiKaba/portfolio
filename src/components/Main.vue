<template>
    <div class="main-container">
        <div class="cover"> 
            <Navbar></Navbar>
            <img class="mx-auto" src="../assets/svg_folder/wave.svg" alt="wave">  
            <main>
                <div class="title mt-5 py-5">
                    <p class="white para1 ">Hello, My Name is</p>
                    <h1 class="white">FADI KABA</h1>
                    <p class="white para2">Backend and frontend web developer</p>
                    <button class="btn btn-light">Contact me</button>
                </div>
                     <Carous></Carous>  
            </main>         
        </div>





    </div>
</template>
<script>

import Navbar from './Navbar';
import Carous from './Carous';

export default {
    name:'Main',
    data: function(){
        return{
            
        }
    },
    components:{
        Navbar, Carous
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
       font-family: sans-serif;
       .cover{
          background-color: $color1; 
          height: 90vh;
          position:relative;
          img{
              position:absolute;
              bottom:0;
              left:0;
              width: 100vw;
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
              button{
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
</style>