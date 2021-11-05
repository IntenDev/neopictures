<template>
  <words-page />
</template>

<script>
import WordsPage from '~/components/WordsPage'
export default {
  name: 'words',
  components: { WordsPage },
  head: {
    title: 'Неокартины художника Алексея Анисимова | Слова',
    meta: [
      {
        hid: 'description',
        name: 'desсription',
        content: 'Слова - на этой странице цитаты известных людей в адрес художника Алексея Анисимова'
      }
    ]
  }
}
</script>
<style scoped>
</style>
