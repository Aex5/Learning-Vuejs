<template>
  <h1>welcome {{name}} !</h1>
  <button v-on:click="changeName">change name</button>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      name: "aditya"
    }
  },
  methods: {
    changeName(){
      this.name = "sujarwo tejo"
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
