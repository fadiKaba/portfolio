<template>
    <div class="">
    <!-- <nav :class="['navbar fixed-top navbar-expand-lg', isNotTop ? 'not-top' : 'now-top']">
        <div class="container">
            <a :class="['navbar-brand text-light', isNotTop ? 'font-big':'font-normal']" href="#">fadikaba</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon">tt</span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ml-auto">
                <li class="nav-item mx-md-3">
                <a class="nav-link text-light" aria-current="page" href="#">Home</a>
                </li>
                <li class="nav-item mx-md-3">
                <a class="nav-link text-light" href="#">Features</a>
                </li>
                <li class="nav-item mx-md-3">
                <a class="nav-link text-light" href="#">Pricing</a>
                </li>
            </ul>
            </div>
        </div>
    </nav> -->
    <div>
  <b-navbar toggleable="lg"  :class="['navbar fixed-top navbar-expand-lg', isNotTop? 'is-not-top': 'is-top']">
    <b-navbar-brand href="#" :class="['navbar-brand']">fadikaba</b-navbar-brand>
    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        
      </b-navbar-nav>

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
          <b-nav-item href="#" class="">Home</b-nav-item>
          <b-nav-item href="#" class="white">Features</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</div>
    </div>
</template>
<script>

export default {
    name:'Navbar',
    props:[],
    data: function(){
        return{
            isNotTop: false,
        }
    },
    mounted: function(){
        this.changeIstop();
        console.log()
    },
    methods:{
       changeIstop: function(){
          let th = this;
          window.document.body.onscroll = function(){
            th.he();
         }
      },
      he: function(){
            let top = Math.abs(document.body.getBoundingClientRect().y);
           if(top > 100){
             this.isNotTop = true;
           }else{
               this.isNotTop = false;
           }
      }
    }
}
</script>
<style lang="scss" scoped>
$color1:#488CEA;
$color2: rgb(255, 203, 5);
nav{
    
    background-color: $color1;
}
.navbar-light .navbar-nav .nav-link, .navbar-light .navbar-brand{
    color:#fff;
    &:hover{
        color:$color2;
    }
}
.font-normal{
    transition: 0.4s;
    font-size: 2rem;
}
.is-top{
  animation: in 0.5s forwards;
}
.is-not-top{
  animation: out 0.5s forwards;
}
@keyframes in {
    0%{
        height: 45px; 
        border-bottom: solid 2px rgb(57, 121, 209);
    }
    100%{
        height: 60px;
        border:none;
    }
}
@keyframes out{
    0%{
        height: 60px;
        border:none;
    }
    100%{
        height: 45px;
        border-bottom: solid 2px rgb(57, 121, 209);
    }
}
</style>