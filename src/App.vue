<template>
  <div id="app">
    <!-- <NavBar/> -->
    <NavTwo/>
    <Banner/>
    <Mission/>
  </div>
</template>

<script>
import Banner from "./components/Banner"
// import NavBar from "./components/NavBar"
import Mission from "./components/Missions"
import NavTwo from "./components/NavTwo"
export default {
  name: 'App',
  components: {
    // NavBar,
    Banner,
    Mission,
    NavTwo
  }
}
</script>

<style>
@font-face{
  font-family: "futura";
  src:local("futura"),
  url(./fonts/Futura-PT/FuturaPTBook.otf)format("truetype");
}
@font-face{
  font-family: "futura-light";
  src:local("futura-light"),
  url(./fonts/Futura-PT/FuturaPTLight.otf)format("truetype");
}
@font-face{
  font-family: "futura-medium";
  src:local("futura-medium"),
  url(./fonts/Futura-PT/FuturaPTMedium.otf)format("truetype");
}
*{
  margin:0px;
  padding:0px;
  box-sizing: border-box;
}
</style>
