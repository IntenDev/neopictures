<template>
  <div class="container">
    <div class="row">
      <div class="main col">
        <NuxtLink to="/">
          ГЛАВНАЯ
        </NuxtLink>
        <br>
        <NuxtLink to="/gallery">
          ГАЛЕРЕЯ
        </NuxtLink>
        <br>
        <NuxtLink to="/words">
          СЛОВА
        </NuxtLink>
        <br>
        <NuxtLink to="/contact">
          КОНТАКТ
        </NuxtLink>
        <br>
      </div>
      <div class="author col">
        НЕОКАРТИНЫ <span>АЛЕКСЕЯ АНИСИМОВА<sup>Ѓ</sup></span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>

</style>
