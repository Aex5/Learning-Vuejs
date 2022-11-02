<template>
  <a v-bind:href="url">Go To Link</a><br>
  <input type="text" v-model="nama">
  {{nama}} <br>

<div v-if="products.length"> 
  <ul>
    <li v-for="item in products" :key="item.id">{{item.id}} - {{item.model}} - {{item.price}}</li>
  </ul>
</div>

<div v-else>
  <p>Product Not Found</p>
</div>
 
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      url: "https://www.google.com",
      nama: "adit",
      products: [
        {id:1, model: "pc", price: 10000},
        {id:2, model: "pc", price: 20000},
        {id:3, model: "pc", price: 30000},
        {id:4, model: "pc", price: 40000},
        {id:5, model: "pc", price: 50000},
      ]
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
