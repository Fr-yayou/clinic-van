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
}
.heroImage{
    height: 600px;
    background-repeat: no-repeat;
    background-size: cover;
    opacity: 0.6;
    background-position: center;
    

}

</style>