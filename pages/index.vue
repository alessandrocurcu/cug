<template>
  <section>
    <the-book :book="book"></the-book>
  </section>
</template>

<script>
import BookData from '../book.json'
import TheBook from '@/components/TheBook'
export default {
  name: 'HomePage',
  components: {
    TheBook,
  },
  data() {
    return {
      book: BookData,
    }
  },
}
</script>
