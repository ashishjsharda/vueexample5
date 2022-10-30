<template>
  <div id="app">

    <Greeting :greeting="greeting" :who="who"/>
  </div>
</template>

<script>
import Greeting from "./components/Greeting";

export default {

  components: {
    Greeting
  },

  data() {
    return {
      greeting: "Hello",
      who: "Vue"
    };
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
