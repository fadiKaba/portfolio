<template>
    <div class="border-bottom py-4" id="skills">
        <h3 class="blue-title">Knowledge & skills</h3>
        <div class="mt-2 mt-md-5 progress-bars">
            <div class=" mb-2 mb-md-4">
                <div>
                    <img class="d-flex mr-auto mb-2" src="../assets/iconic/html.png" width="50px" alt="html">
                </div>
                 <div class="progress" style="height: 30px;">
                    <div class="progress-bar" role="progressbar"  aria-valuenow="25" aria-valuemin="0" aria-valuemax="100">
                        <span class="font-weight-bold">90%</span>
                    </div>
                </div>
            </div>
            <div class="mb-2 mb-md-4">
                <div>
                    <img class="d-flex mr-auto mb-2" src="../assets/iconic/css.png" width="50px" alt="html">
                </div>
                 <div class=" progress" style="height: 30px;">
                    <div class="progress-bar" role="progressbar" style="width: 85%;" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100">
                        <span class="font-weight-bold">85%</span>
                    </div>
                </div>
            </div>
            <div class="mb-2 mb-md-4">
                <div>
                    <img class="d-flex mr-auto mb-2" src="../assets/iconic/js.png" width="50px" alt="html">
                </div>
                 <div class=" progress" style="height: 30px;">
                    <div class="progress-bar" role="progressbar" style="width: 80%;" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100">
                        <span class="font-weight-bold">80%</span>
                    </div>
                </div>
            </div>
            <div class="mb-2 mb-md-4">
                <div>
                    <img class="d-flex mr-auto mb-2" src="../assets/iconic/php.png" width="50px" alt="html">
                </div>
                 <div class="progress" style="height: 30px;">
                    <div class="progress-bar" role="progressbar" style="width: 80%;" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100">
                        <span class="font-weight-bold">80%</span>
                    </div>
                </div>
            </div>
        </div>
        <div class="mt-3 mb-3 mt-md-5 mb-md-5">
            <h3 class="blue-title">Frameworks & libraries</h3>
            <div class="row mt-2 mt-md-5">
                <div class="col-md-3 my-3"><img src="../assets/iconic/laravel.png" alt="laravel" width="60%"></div>
                <div class="col-md-3 my-3"><img src="../assets/iconic/vue-js.png" alt="laravel" width="60%"></div>
                <div class="col-md-3 my-3"><img src="../assets/iconic/bootstrap.png" alt="laravel" width="60%"></div>
                <div class="col-md-3 my-3"><img src="../assets/iconic/sass.png" alt="laravel" width="60%"></div>
            </div>
        </div>
        <div class="languages-bar">
            <h3 class="blue-title">Foreign languages</h3>
            <div class="mb-2 mb-md-4">
                <div>
                    <span class="blue-title d-flex mr-auto">English</span>
                </div>
                 <div class="progress" style="height: 30px;">
                    <div class="progress-bar language-bar" role="progressbar" style="width: 75%;" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100">
                        <span class="font-weight-bold">75%</span>
                    </div>
                </div>
            </div>
            <div class="mb-2 mb-md-4">
                <div>
                    <span class="blue-title d-flex mr-auto">Frensh</span>
                </div>
                 <div class="progress" style="height: 30px;">
                    <div class="progress-bar language-bar" role="progressbar" style="width: 60%;" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100">
                        <span class="font-weight-bold">60%</span>
                    </div>
                </div>
            </div>
            <div class="mb-2 mb-md-4">
                <div>
                    <span class="blue-title d-flex mr-auto">Arabic</span>
                </div>
                 <div class="progress" style="height: 30px;">
                    <div class="progress-bar language-bar" role="progressbar" style="width: 100%;" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100">
                        <span class="font-weight-bold">100%</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name:'Skills',
    data: function(){
        return {
            html:0,
            css:0,
            js:0,
            php:0
        }
    },
    mounted: function(){
        this.scroll();
    },
    methods:{
        scroll: function(){
            let th = this;
            window.document.body.onscroll = function(){
            th.he();
           }
        },
        he: function(){
            let progressBars = document.querySelector('.progress-bars').getBoundingClientRect();
            let bars = document.querySelectorAll('.progress-bars .progress-bar');
            let percentage = document.querySelectorAll('.progress-bars .progress-bar > span');

            let languagesBars = document.querySelector('.languages-bar').getBoundingClientRect();
            let lBars = document.querySelectorAll('.languages-bar .language-bar');
            let lPercentage = document.querySelectorAll('.languages-bar .progress-bar > span');
            
            if(progressBars.top < window.innerHeight && progressBars.bottom >= 0) {
                bars[0].classList.add('html-bar');
                bars[1].classList.add('css-bar');
                bars[2].classList.add('js-bar');
                bars[3].classList.add('php-bar');
                percentage.forEach(item => {
                    item.classList.add('bar-percentage');
                })
            }

            if(languagesBars.top < window.innerHeight && languagesBars.bottom >= 0) {
               lBars[0].classList.add('english-bar');
               lBars[1].classList.add('frensh-bar');
               lBars[2].classList.add('arabic-bar');
               lPercentage.forEach(item => {
                    item.classList.add('bar-percentage');
                })
            }
        }
    }
}
</script>
<style lang="scss" scoped>

$color1:#488CEA;
.progress-bar{
    background-color: $color1;
}

.html-bar{
    animation: html 1.5s forwards;
}
.css-bar{
    animation: css 1.5s forwards;
}
.js-bar{
    animation: js 1.5s forwards;
}
.php-bar{
    animation: php 1.5s forwards;
}
.english-bar{
    animation: english 1.5s forwards;
}
.frensh-bar{
    animation: frensh 1.5s forwards;
}
.arabic-bar{
    animation: arabic 1.5s forwards;
}
.bar-percentage{
    animation: show 1.5s forwards;
}

@keyframes show {
    0%{
        opacity: 0;
    }
    95%{
        opacity: 0;
    }
    100%{
        opacity: 1;
    }
}
@keyframes html{
    0%{
        width: 0;
    }
    100%{
        width: 90%;
    }
}
@keyframes css{
    0%{
        width: 0;
    }
    100%{
        width: 85%;
    }
}
@keyframes js{
    0%{
        width: 0;
    }
    100%{
        width: 80%;
    }
}
@keyframes php{
    0%{
        width: 0;
    }
    100%{
        width: 80%;
    }
}
@keyframes english{
    0%{
        width: 0;
    }
    100%{
        width: 75%;
    }
}
@keyframes frensh{
    0%{
        width: 0;
    }
    100%{
        width: 60%;
    }
}
@keyframes arabic{
    0%{
        width: 0;
    }
    100%{
        width: 100%;
    }
}
</style>