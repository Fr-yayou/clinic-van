<template>
  <div class="container-heroImage" :style="{backgroundImage:`url('${imageHero}')`}">
      <div class="container-text">
          <p>We are here to improve the community's</p>
          <br>
          <p>Physical health, mental health,</p>
          <br>
          <p>sports performance and</p>
          <br>
          <p>quality of life.</p>
      </div>
  </div>
</template>

<script>
import imageHero from "../assets/hero.png"
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
    height: 400px;
    overflow: hidden;
    position: relative;
    background-repeat: no-repeat;
    background-size: 100%;
    background-position: top left; 
}


@media screen and (min-width:768px){
    .container-heroImage{
        height: 700px;
        background-size: 100%;
        background-position: top left; 

    }
    .container-text{
        position: absolute;
        top: 50%;
        left: 40%;
        transform: translate(-50%, -50%);
    }
    .container-text p{
        color:#001b36;
        font-size:35px;
        background-color:white;
        margin-bottom: 5px;
        display: inline-block
    }
}

</style>