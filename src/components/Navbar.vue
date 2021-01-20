<template>
    <div class="">
    <nav :class="isFixed ? 'navbar fixed-top navbar-expand-lg' : 'navbar navbar-expand-lg'">
        <div class="container">
            <a class="navbar-brand text-light" href="#">fadikaba</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
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
    </nav>
    </div>
</template>
<script>
export default {
    name:'Navbar',
    props:['isFixed']
}
</script>
<style lang="scss" scoped>
$color1:#488CEA;
nav{
    border-bottom: solid 2px rgb(57, 121, 209);
    background-color: $color1;
}
</style>