<template>
  <div id="app">
    <NavBar/>
    <Banner/>
    <Mission/>
  </div>
</template>

<script>
import Banner from "./components/Banner"
import NavBar from "./components/NavBar"
import Mission from "./components/Missions"
export default {
  name: 'App',
  components: {
    NavBar,
    Banner,
    Mission
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
