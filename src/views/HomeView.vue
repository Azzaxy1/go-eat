<template>
  <div class="d-flex justify-content-center align-items-center">
    <div class="container">
      <Hero />
      <BestFoods :products />
    </div>
  </div>
</template>

<script>
import Hero from '@/components/Hero.vue'
import BestFoods from '@/components/BestFoods.vue'
import axios from 'axios'

export default {
  name: 'HomeView',
  components: {
    Hero,
    BestFoods,
  },
  data() {
    return {
      products: [],
    }
  },

  methods: {
    setProducts(data) {
      this.products = data
    },
  },

  mounted() {
    axios
      .get('http://localhost:3000/best-products')
      .then((res) => this.setProducts(res.data))
      .catch((err) => console.log(err))
  },
}
</script>
