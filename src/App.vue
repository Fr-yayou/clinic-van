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
*{
  margin:0px;
  padding:0px;
  box-sizing: border-box;
}
</style>
