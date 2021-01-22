<template>
    <div>
        <div class="row top-f p-1 p-md-5">
             <div class="col-md-6">
                 <ul>
                     <li class="text-left my-1"><span>Fadi Kaba</span></li>
                     <li class="text-left my-1">I am a nice guy who can help you to achieve what you are looking for</li>
                     <li class="text-left my-1">I have a firm dedication to the company values</li>
                     <li class="text-left my-1">I can prioritize projects and tasks</li>
                     <li class="text-left my-1">Working to hold high standards for self and for others on the team</li>
                 </ul>
             </div>
             <div class="col-md-3">
                 <ul>
                     <li class="text-left my-1"><span>Menu</span></li>
                     <li class="text-left my-1"><a href="#skills">Skills</a></li>
                     <li class="text-left my-1"><a href="#about">About</a></li>
                     <li class="text-left my-1"><a href="#portfolio">Portfolio</a></li>
                 </ul>
             </div>
             <div class="col-md-3">
                 <ul>
                     <li class="text-left my-1"><span>Social Media</span></li>
                     <li class="text-left my-2">
                        <a href="https://www.facebook.com/fadi.kaba.14" target="_blank">
                            <img src="../assets/iconic/facebook.png" width="30px" alt="FB">
                        </a>
                    </li>
                     <li class="text-left my-2">
                         <a href="https://github.com/fadiKaba" target="_blank">
                            <img src="../assets/iconic/github.png" width="30px" alt="github">
                        </a>
                     </li>
                     <li class="text-left my-2">
                         <a href="https://www.instagram.com/fsdikaba85/?hl=en" target="_blank">
                            <img src="../assets/iconic/instagram.png" width="30px" alt="instagram">
                        </a>
                     </li>
                 </ul>
             </div>
        </div>
        <div class="bot-f">
            <p class="py-2 ">Fadi Kaba &copy; 2021 All rights reserved</p>
        </div>
    </div>
</template>
<script>
export default {
    name: 'Footer',
}
</script>
<style lang="scss" scoped>
$color2: rgb(255, 203, 5);
     .top-f{
       background-color: #043769;
       color: #808080;
       span{
           font-weight: bold;
           font-size: 1.2rem;
           color:#fff;
       }
       li{
         a{
             color:grey;
             img{
                 &:hover{
                     transition: 0.2s;
                     transform: scale(1.1);
                 }
             }
         }
       }
     }
     .bot-f{
        background-color: $color2;  
        color:#fff;
     }
</style>