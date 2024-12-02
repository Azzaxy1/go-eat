<template>
  <div>
    <b-card
      :title="product.nama"
      :img-src="'/src/assets/img/' + product.gambar"
      :img-alt="product.nama"
      img-top
      tag="article"
      style="max-width: 20rem"
      class="mb-2 shadow"
    >
      <b-card-text>
        {{ product.harga }}
      </b-card-text>

      <b-button href="#" variant="success">
        <img src="../assets/img/cart.png" alt="cart" width="20" />
        Masukan Keranjang
      </b-button>
    </b-card>
  </div>
</template>
<script>
export default {
  name: 'CardProduct',
  props: ['product'],
}
</script>
