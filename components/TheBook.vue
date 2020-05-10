<template>
  <article class="columns">
    <div class="column is-narrow">
      <p>{{ book.title }}</p>
      <div>
        <ul>
          <li v-for="(authorName, i) in book.authorsName" :key="i">
            di {{ authorName }}
          </li>
        </ul>
      </div>
      <img
        :src="require(`../assets/img/${book.img.toLowerCase()}`)"
        :alt="book.imgAlt"
      />
      <p>{{ book.publishedAt }}</p>
      <p>{{ book.paperFormat }}</p>
      <p>{{ book.pages }}</p>
      <p>{{ book.ISBN }}</p>
    </div>
    <div class="column is-three-fifths" style="margin-top: 4rem;">
      <p>{{ book.subTitle }}</p>
      <p>{{ book.shortDescription }}</p>
      <div style="display: flex;">
        <div>
          <p>{{ book.pricePaper }} €</p>
          <button
            class="snipcart-add-item"
            :data-item-id="book.id"
            :data-item-price="book.pricePaper"
            :data-item-url="bookUrl"
            :data-item-image="
              require(`../assets/img/${book.img.toLowerCase()}`)
            "
            :data-item-description="book.subTitle"
            :data-item-name="book.title"
            data-item-has-taxes-included="true"
          >
            Acquista il libro cartaceo
          </button>
        </div>
        <div style="margin-left: 5%;">
          <p>{{ book.priceEbook }} €</p>
          <button>
            Acquista l'ebook
          </button>
        </div>
      </div>
    </div>
  </article>
</template>

<script>
export default {
  name: 'TheBook',
  props: {
    book: {
      type: Object,
      default: () => {},
    },
  },
  computed: {
    bookUrl() {
      return this.$route.path
    },
  },
}
</script>

<style lang="scss" scoped></style>
