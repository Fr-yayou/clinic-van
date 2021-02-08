<template>
  <div id="app">
    <NavBar/>
    <Banner/>
  </div>
</template>

<script>
import Banner from "./components/Banner"
import NavBar from "./components/NavBar"
export default {
  name: 'App',
  components: {
    NavBar,
    Banner
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
