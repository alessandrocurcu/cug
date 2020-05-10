<template>
  <div>
    <section class="section">
      <h1>{{ snip }}</h1>
      <div class="container">
        <div style="text-align: right;">
          <a href="#" class="snipcart-checkout">Vedi carrello</a>
          • Nel carrello ci sono
          <span class="snipcart-items-count"></span> libri per un totale di
          <span class="snipcart-total-price"></span>
        </div>
        <nuxt />
      </div>
    </section>
    <div id="snipcart" hidden :data-api-key="snipcartApiPublicKey"></div>
    <script src="https://cdn.snipcart.com/themes/v3.0.12/default/snipcart.js"></script>
  </div>
</template>

<script>
export default {
  computed: {
    snipcartApiPublicKey() {
      return process.env.SNIPCART
    },
  },
}
</script>
