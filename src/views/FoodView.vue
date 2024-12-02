<template>
  <div class="container">
    <div class="row mt-4">
      <div class="col">
        <h1>Daftar <strong class="text-success">Makanan</strong></h1>
        <div class="my-3">
          <b-form-input
            v-model="searchQuery"
            @input="handleSearchFood"
            placeholder="Cari makanan"
          ></b-form-input>
        </div>
      </div>
    </div>

    <div class="row">
      <div class="col-md-4 mb-3" v-for="(product, i) in products" :key="i">
        <CardProduct :product />
      </div>
    </div>
  </div>
</template>

<script>
import CardProduct from '@/components/CardProduct.vue'
import axios from 'axios'

export default {
  components: {
    CardProduct,
  },

  data() {
    return {
      products: [],
      searchQuery: '',
    }
  },

  methods: {
    setProducts(data) {
      this.products = data
    },
    handleSearchFood() {
      axios
        .get(`http://localhost:3000/products?q=${this.searchQuery}`)
        .then((res) => this.setProducts(res.data))
    },
  },

  mounted() {
    axios
      .get('http://localhost:3000/products')
      .then((res) => this.setProducts(res.data))
      .catch((err) => console.log(err))
  },
}
</script>
