<template>
  <div>
    <section class="section">
      <div class="container">
        <a href="#" class="is-pulled-right">Vedi carrello</a>
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
