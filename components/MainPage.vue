<template>
  <div id="app">
    <div class=" container">
      <div class="row">
        <div class="main col">
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

    <img class="pechat" src="~/assets/images/pechat.png" width="25" height="22">
    <div id="author">
      <img src="~/assets/images/author1.png" class="center">
    </div>
  </div>
</template>

<script>
export default {
  name: 'MainPage'
}
</script>
<style scoped>
</style>
