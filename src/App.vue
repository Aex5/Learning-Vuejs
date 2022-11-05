<script>
import Header from '@/components/Header.vue'


export default {
  name: "App",
  components: {
    Header
  },

  data() {
    return {
      cari: "",
      data: "ini adalah text via props app.vue",
      url: "https://www.google.com",
      nama: "sujarwo tejo",
      products: [
       
      ],
    };
  },

  created() {
    this.products = [
        { id: 1, model: "example1", price: 10000 },
        { id: 2, model: "exmaple2", price: 20000 },
        { id: 3, model: "exmaple3", price: 30000 },
        { id: 4, model: "exmaple4", price: 40000 },
        { id: 5, model: "exmaple4", price: 50000 },
    ]
  },

  computed: {
    cariData(){
      return this.products.filter((item) => {
        return item.model.match(this.cari)
      })
    }
  }
};
</script>

<template>
  <Header text="ini adalah text via props dari app.vue"/>

  <a v-bind:href="url">Go To Link</a><br />
  <input type="text" v-model="cari" placeholder="search"/>
  {{ nama }} <br />

  <div v-if="products.length">
    <ul>
      <li v-for="item in cariData" :key="item.id">
        {{ item.id }} - {{ item.model }} - {{ item.price }}
      </li>
    </ul>
  </div>

  <div v-else>
    <p>Product Not Found</p>
  </div>
</template>

<style>

</style>
