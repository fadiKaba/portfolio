<template>
    <div class="">
    <div>
        <b-navbar toggleable="lg"  :class="['navbar fixed-top navbar-expand-lg px-md-5', isT? 'is-not-top': 'is-top']">
            <b-navbar-brand href="#" ><img width="25px" src="../assets/iconic/contact.png" alt="@"> <span class="text-light">Fadi</span><span :class="['navbar-brand', isT ? 'text-warning' : '']">Kaba</span> </b-navbar-brand>
            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" :class="isT? 'is-not-top': 'is-top'" is-nav>
            <b-navbar-nav>
                
            </b-navbar-nav>

            <!-- Right aligned nav items -->
            <b-navbar-nav class="ml-auto">
                <b-nav-item href="#skills" class="mx-md-2 nav-b-item">SKILLS</b-nav-item>
                <b-nav-item href="#about" class="mx-md-2 nav-b-item">About</b-nav-item>
                <b-nav-item href="#portfolio" class="mx-md-2 nav-b-item">Portfolio</b-nav-item>
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
    created:function(){
      this.changeIstop();
    },
    destroyed: function(){
        
        console.log()
    },
    methods:{
       changeIstop: function(){
            let th = this;
            window.addEventListener('scroll', function(){
                let top = Math.abs(document.body.getBoundingClientRect().y);
                if(top > 100){
                    th.isNotTop = true;
                }else{
                    th.isNotTop = false;
                }
            }
            )
       },
      he: function(){
            let top = Math.abs(document.body.getBoundingClientRect().y);
           if(top > 50){
               console.log(this.isNotTop)
             this.isNotTop = true;
           }else{
               this.isNotTop = false;
           }
      }
    },
    computed:{
        isT: function(){
            return this.isNotTop;
        }
    }
}
</script>
<style lang="scss" scoped>
$color1:#488CEA;
$color2: #ffcb05;
$color3: #043769;
nav{   
    background-color: $color1;
    font-family: 'open-sans', sans-serif;
    .navbar-collapse{
       background-color: $color3;
    }
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
.nav-b-item{
    text-transform: uppercase;
}
.yellow{
    color:$color2;
    text-transform: capitalize;
}
@keyframes in {
    0%{
      //  border-bottom: solid 2px rgb(57, 121, 209);
        background-color: $color3 ;
    }
    100%{
        border:none;
        background-color: $color1 ;
    }
}
@keyframes out{
    0%{
        background-color: $color1 ;
    }
    100%{
        background-color: $color3 ;
      //  border-bottom: solid 2px rgb(57, 121, 209);
    }
}
</style>