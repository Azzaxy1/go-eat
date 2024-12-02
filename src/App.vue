<template>
  <Navbar />
  <RouterView />
  <FooterSection />
</template>

<script>
import Navbar from './components/Navbar.vue'
import FooterSection from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    FooterSection,
  },
}
</script>
