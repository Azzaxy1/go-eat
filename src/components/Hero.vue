<template>
  <div class="row">
    <div class="col d-flex justify-content-center flex-column">
      <h2>
        <strong>Delicious Food Menu, </strong> <br />
        in Your Gadget
      </h2>
      <p>Ayo segera pilih dan pesan makanan favorit anda</p>
      <router-link class="btn w-25 btn-success">
        <ArrowIcon />
        Pesan
      </router-link>
    </div>
    <div class="col d-flex justify-content-center">
      <img src="../assets/hero.svg" alt="hero" width="400" />
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
