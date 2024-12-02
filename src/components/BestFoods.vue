<template>
  <div class="row mt-4 vh-100">
    <div class="col">
      <h1>Best <strong>Foods</strong></h1>
    </div>
    <div class="col">
      <router-link to="/foods" class="btn btn-success float-end">
        <img src="../assets/img/eye.png" alt="eye" width="20" />
        Lihat Semua
      </router-link>
    </div>

    <div class="row mb-3">
      <div class="col-md-4 mt-4" v-for="product in products" :key="product.id">
        <CardProduct :product />
      </div>
    </div>
  </div>
</template>

<script>
import CardProduct from './CardProduct.vue'

export default {
  name: 'BestFoods',
  components: {
    CardProduct,
  },
  props: ['products'],
}
</script>
