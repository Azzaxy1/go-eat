<template>
  <b-navbar toggleable="lg" variant="light" type="light" class="sticky-top">
    <div class="container">
      <div class="d-flex">
        <b-navbar-brand href="/" class="mt-2 fs-3 fw-semibold"
          >Go<span class="text-success">Eat</span></b-navbar-brand
        >

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav class="w-100 d-flex justify-content-end">
            <b-nav-item>
              <router-link
                to="/"
                class="nav-link"
                :class="{ 'text-success fw-bold': isActive('/') }"
                >Home</router-link
              >
            </b-nav-item>
            <b-nav-item>
              <router-link
                to="/about"
                class="nav-link"
                :class="{ 'text-success fw-bold': isActive('/about') }"
                >About</router-link
              >
            </b-nav-item>
            <b-nav-item>
              <router-link
                to="/foods"
                class="nav-link"
                :class="{ 'text-success fw-bold': isActive('/foods') }"
                >Order Makanan</router-link
              >
            </b-nav-item>
          </b-navbar-nav>

          <b-navbar-nav class="w-75 d-flex justify-content-end">
            <b-nav-item>
              <router-link to="/keranjang" class="nav-link"
                >Keranjang
                <IconBag />
                <span class="badge text-bg-success ms-2">0</span>
              </router-link>
            </b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </div>
    </div>
  </b-navbar>
</template>

<script>
import IconBag from './icons/IconBag.vue'

export default {
  name: 'NavigationBar',
  components: {
    IconBag,
  },
  methods: {
    isActive(route) {
      return this.$route.path === route
    },
  },
}
</script>

<style></style>
