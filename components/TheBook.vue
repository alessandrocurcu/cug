<template>
  <article>
    <div>
      <ul>
        <li v-for="(authorName, i) in book.authorsName" :key="i">
          {{ authorName }}
        </li>
      </ul>
    </div>
    <p>{{ book.title }}</p>
    <p>{{ book.subTitle }}</p>
    <p>{{ book.img }}</p>
    <p>{{ book.publishedAt }}</p>
    <p>{{ book.shortDescription }}</p>
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
}
</script>

<style lang="scss" scoped></style>
