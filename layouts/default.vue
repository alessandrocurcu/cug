<template>
  <div>
    <section class="section">
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
    <div
      id="snipcart"
      hidden
      data-api-key="MDI0N2M1MmUtZDY0NC00ODRmLWExNzYtMjliZmRlZTQwN2Y4NjM3MTcxMjQ3ODMyOTc1NjMy
"
    ></div>
    <script src="https://cdn.snipcart.com/themes/v3.0.12/default/snipcart.js"></script>
  </div>
</template>

<script>
export default {}
</script>
