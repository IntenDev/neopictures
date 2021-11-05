<template>
  <gallery-page />
</template>

<script>
import GalleryPage from '~/components/GalleryPage'
export default {
  name: 'Gallery',
  components: { GalleryPage },
  head: {
    title: 'Неокартины художника Алексея Анисимова | Галерея',
    meta: [
      {
        hid: 'description',
        name: 'desсription',
        content: 'Серия неокартин - «Юная Иволга», холст, акрил, авторская техника 2014 год. Художник Алексей Анисимов.'
      }
    ]
  }
}
</script>

<style scoped>

</style>
