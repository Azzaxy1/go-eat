<template>
  <div>
    <b-card
      :title="product.nama"
      :img-src="'/src/assets/img/' + product.gambar"
      :img-alt="product.nama"
      img-top
      img-height="220"
      tag="article"
      style="max-width: 20rem"
      class="mb-2 shadow"
    >
      <b-card-text class="text-success"> Rp.{{ product.harga }} </b-card-text>

      <b-button href="#" variant="success">
        <img src="../assets/img/cart.png" alt="cart" width="20" />
        Pesan
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
