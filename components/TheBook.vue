<template>
  <article>
    <div>
      <ul>
        <li v-for="(authorName, i) in book.authorsName" :key="i">
          di {{ authorName }}
        </li>
      </ul>
    </div>
    <p>{{ book.title }}</p>
    <img src="@/assets/img/alice.jpg" />
    <p>{{ book.publishedAt }}</p>
    <p>{{ book.paperFormat }}</p>
    <p>{{ book.pages }}</p>
    <p>{{ book.ISBN }}</p>
    <p>{{ book.subTitle }}</p>
    <p>{{ book.shortDescription }}</p>
    <p>{{ book.pricePaper }} €</p>
    <button>Acquista il libro cartaceo</button>
    <p>{{ book.priceEbook }} €</p>
    <button>Acquista l'ebook</button>
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
