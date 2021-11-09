<template>
  <div>
    <main-page />
  </div>
</template>

<script>
import MainPage from '~/components/MainPage'
export default {
  components: { MainPage },
  head: {
    title: 'Неокартины художника Алексея Анисимова | Главная',
    meta: [
      {
        hid: 'description',
        name: 'desсription',
        content: 'Неокартины - уникальный интеллектуально-художественный продукт, синтезирующий изобразительное искусство, дизайн и поэзию.'
      }
    ]
  }
}
</script>
<style scoped>

</style>
