<template>
    <div class="my-3 my-md-5" id="portfolio">
        <h3 class="blue-title">Portfolio</h3>
         <div class="mt-2 mt-md-4 list-group">
            <a class="list-group-item list-group-item-action border-0" aria-current="true">
                <div class="d-flex w-100 justify-content-between">
                    <h5 class="mb-1 text-left">
                        <img class="mr-2 mr-md-4" width="25px" src="../assets/iconic/circle.png" alt="-">
                        Personal projects (web development related)
                    </h5>
                </div>
                <p class="mb-1 text-left">Personal websites (2020):
                    <ul class="ml-auto web-related">
                        <li>
                            <div class="row p-2 p-md-5">
                                <div class="col-md-3 d-flex align-items-center">
                                     <a href="http://blife.dx.am/" class="font-weight-bold">http://blife.dx.am/</a> 
                                </div>
                                <div class="col-md-9 rounded">
                                    <a href="http://blife.dx.am/"><img class="rounded" src="../assets/images/blife.jpg" width="100%" alt="blife"></a>
                                </div>
                            </div>
                        </li>
                        <li>
                            <div class="row p-2 p-md-5">
                                <div class="col-md-3 d-flex align-items-center">
                                     <a href="https://fadik.dx.am" class="font-weight-bold">https://fadik.dx.am</a> 
                                </div>
                                <div class="col-md-9 rounded">
                                    <a href="https://fadik.dx.am"><img class="rounded" src="../assets/images/fkdev.jpg" width="100%" alt="fadik"></a>
                                </div>
                            </div>
                        </li>
                    </ul>
                </p>
            </a>
             <a class="list-group-item list-group-item-action border-0">
                <div class="d-flex w-100 justify-content-between">
                <h5 class="mb-1 text-left"><img class="mr-2 mr-md-4" width="25px" src="../assets/iconic/circle.png" alt="-"> Mimosa for laboratory equipment  (2019 - 2021)</h5>
                </div>
                <p class="mb-1">Worked as a storekeeper</p>
            </a>
            <a class="list-group-item list-group-item-action border-0">
                <div class="d-flex w-100 justify-content-between">
                <h5 class="mb-1 text-left"><img class="mr-2 mr-md-4" width="25px" src="../assets/iconic/circle.png" alt="-"> Sabagh corporation (2008-2009)</h5>
                </div>
                <p class="mb-1">Worked as an administrative dispatcher</p>
            </a>
            <a class="list-group-item list-group-item-action border-0">
                <div class="d-flex w-100 justify-content-between">
                <h5 class="mb-1 text-left"><img class="mr-2 mr-md-4" width="25px" src="../assets/iconic/circle.png" alt="-"> Doha Beton Company (2004-2007)</h5>
                </div>
                <p class="mb-1">Worked as an administrative dispatcher</p>
            </a>  
        </div>
    </div>
</template>
<script>
export default {
    name: 'Exprience',
    mounted: function(){
      this.chScale(document.querySelectorAll('.web-related li div img'));
    },
    methods:{
        chScale: function(items){
            items.forEach(element => {
                element.addEventListener('mouseover', function(){
                    element.classList.remove('scale-change-out');
                    element.classList.add('scale-change-in');
                });
                 element.addEventListener('mouseout', function(){
                    element.classList.remove('scale-change-in');
                    element.classList.add('scale-change-out');
                })
            });
        }
    }
}
</script>
<style lang="scss" scoped>
.web-related{
    li{
        div{
           width: 100%;
           overflow:hidden;
            img{
        }
    }
   
   }
}
.scale-change-in{
    animation: scale 0.3s forwards;
}
.scale-change-out{
    animation: scaleout 0.3s forwards;
}
@keyframes scale{
    0%{
        transform: scale(1);
    }
    100%{
        transform: scale(1.1);
    }
}
@keyframes scaleout{
    0%{
        transform: scale(1.1);
    }
    100%{
        transform: scale(1);
    }
}
</style>