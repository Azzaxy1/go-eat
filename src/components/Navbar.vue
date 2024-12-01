<template>
  <b-navbar toggleable="lg" variant="light" type="light">
    <div class="container">
      <div class="d-flex">
        <b-navbar-brand href="/" class="mt-2 font-bold">GoEat</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item>
              <router-link to="/" class="nav-link">Home</router-link>
            </b-nav-item>
            <b-nav-item>
              <router-link to="/about" class="nav-link">About</router-link>
            </b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </div>
    </div>
  </b-navbar>
</template>

<script>
export default {
  name: 'NavigationBar',
}
</script>

<style></style>
