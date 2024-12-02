<template>
  <div class="row vh-100">
    <div class="col-md-6 order-2 order-md-1 d-flex justify-content-center flex-column">
      <h2>
        <strong class="text-success">Delicious Food Menu, </strong> <br />
        in Your Gadget
      </h2>
      <p>Ayo segera pilih dan pesan makanan favorit anda</p>
      <router-link
        to="/foods"
        class="btn w-25 d-sm-flex justify-content-sm-center flex-column flex-md-row btn-success"
      >
        Pesan
        <ArrowIcon />
      </router-link>
    </div>
    <div class="col-md-6 order-1 order-md-2 d-flex justify-content-center">
      <img src="../assets/img/hero.svg" alt="hero" width="300" class="mb-5 mt-md-0 w-75" />
    </div>
  </div>
</template>
<script>
import ArrowIcon from './icons/ArrowIcon.vue'

export default {
  name: 'HeroSection',
  components: {
    ArrowIcon,
  },
}
</script>
<style lang=""></style>
