<template>
    <div class="my-2 my-md-5 border-bottom py-2 py-md-4" id="about">
        <h2 class="mb-2 mb-md-5 blue-title">About me</h2>
        <div class="card mb-3" style="max-width: 100%;">
            <div class="row g-0">
                <div class="col-md-4">
                <img src="../assets/images/fadi.jpg" alt="fadi kaba" width="100%">
                </div>
                <div class="col-md-8 align-items-center d-flex justify-content-center">
                    <div class="card-body ">
                        <p class="grey-text">I am a stubborn web developer who likes to work hard to achieve his goal, I have a 
                                background in business administration and I had the chance to self-taught about web development in addition 
                                to seeking to obtain an associate degree in computer science.    
                        </p>
                        <p class="grey-text">
                            <span class="blue-text">Name: </span> Fadi Kaba <br>
                            <span class="blue-text">Date of birth:</span> 1/1/1985<br>
                            <span class="blue-text">Address:</span> Damascus/Jaramana<br>
                            <span class="blue-text">Email:</span> fadikaba9@gmail.com<br>
                            <span class="blue-text">Phone:</span> +963940378308
                        </p>
                    </div>
                </div>
            </div>
        </div> 
        <div>
           <h4 class="my-2 my-md-5 blue-title">Education</h4>
           <div class="list-group">
            <a class="list-group-item list-group-item-action border-0" aria-current="true">
                <div class="d-flex w-100 justify-content-between">
                <h5 class="mb-1 text-left"><img class="mr-2 mr-md-4" width="25px" src="../assets/iconic/circle.png" alt="-"> SIUST (Syrian  International University For Science And Technology)</h5>
                </div>
                <p class="mb-1">-Business Administration-Location Damascus 2007-2011</p>
            </a>
            <a class="list-group-item list-group-item-action border-0">
                <div class="d-flex w-100 justify-content-between">
                <h5 class="mb-1 text-left"><img class="mr-2 mr-md-4" width="25px" src="../assets/iconic/circle.png" alt="-"> Damascus University</h5>
                </div>
                <p class="mb-1">-Archaeology-Location Damascus 2002-2003</p>
            </a>
            <a class="list-group-item list-group-item-action border-0">
                <div class="d-flex w-100 justify-content-between">
                <h5 class="mb-1 text-left"><img class="mr-2 mr-md-4" width="25px" src="../assets/iconic/circle.png" alt="-"> UOP (University of the People)</h5>
                </div>
                <p class="mb-1">Working towards an associate degree in Computer Science (Expected to be obtained on 1/12/2021)</p>
            </a>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'About'
}
</script>
<style lang="scss" scoped>

$color1: #488CEA;

.blue-text{
    color:$color1;
    font-size: 1rem;
    text-transform: capitalize;
    font-weight: bold;
}

</style>
