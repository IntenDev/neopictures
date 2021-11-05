<template>
  <contact-page />
</template>

<script>
import ContactPage from '~/components/ContactPage'
export default {
  name: 'contact',
  components: { ContactPage },
  head: {
    title: 'Неокартины художника Алексея Анисимова | Контакты',
    meta: [
      {
        hid: 'description',
        name: 'desсription',
        content: 'Контактная информация художника Алексея Анисимова. Понравились работы? Пишите, я обязательно отвечу.'
      }
    ]
  }
}
</script>

<style scoped>

</style>
