<template>
  <div id="app">

    <Greeting :greeting="greeting" :who="who"/>
    <button @click="newGreeting()">Change Greeting</button>
  </div>
</template>

<script>
import Greeting from "./components/Greeting";

const possibleGreetings=[
  {greeting:"Hello",who:"Vue"},
  {greeting:"Hola",who:"Vue"}
]
export default {

  components: {
    Greeting
  },

  data() {
    return {
      currentIndex:0
    }
  },
  computed:{
    currentGreeting(){
      return possibleGreetings[this.currentIndex]
    },
    greeting(){
      return this.currentGreeting.greeting
    },
    who(){
      return this.currentGreeting.who
    }
  },
  methods:{
    newGreeting(){
      this.currentIndex=this.currentIndex===possibleGreetings.length-1?0:this.currentIndex+1
    }
  }



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
