<template>
  <div class="vh-100 d-flex justify-content-center align-items-center">
    <div class="container">
      <Hero />
    </div>
  </div>
</template>

<script>
import Hero from '@/components/Hero.vue'
import AboutView from './AboutView.vue'

export default {
  name: 'HomeView',
  components: {
    Hero,
    AboutView,
  },
}
</script>
