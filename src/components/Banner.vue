<template>
  <div class="container-heroImage">
      <div class="heroImage" :style="{backgroundImage:`url('${imageHero}')`}"></div>
  </div>
</template>

<script>
import imageHero from "../assets/hero.jpg"
export default {
    name:"Banner",

    data(){
        return{
            imageHero:imageHero
        }
    }
}
</script>

<style scoped>
.container-heroImage{
    background-color: black;
    width: 100%;
    max-width: 100%;
}
.heroImage{
    width: 100%;
    height: 600px;
    overflow: hidden;
    background-repeat: no-repeat;
    background-size: cover;
    opacity:0.8;;
    background-position: center center;
    

}

@media sreen and (max-width:768px){
    .container-heroImage{
        height: 900px;
    }
}

</style>