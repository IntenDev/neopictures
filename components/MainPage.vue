<template>
  <div id="app">
    <div class="main">
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
    <div class="author">
      НЕОКАРТИНЫ <span>АЛЕКСЕЯ АНИСИМОВА<sup>Ѓ</sup></span>
    </div>
    <img class="pechat" src="~/assets/images/pechat.png" width="25" height="22">
  </div>
</template>

<script>
export default {
  name: 'MainPage',
  computed: {
    backgroundStyle () {
      return {
        'background-image': 'url(`@/assets/images/author.png`)',
        'background-repeat': 'no-repeat',
        'background-position': 'center bottom'
      }
    }
  }
}
</script>
<style scoped>
#app {
  width: 100%;
  height: 100%;
  position: absolute;
  background-image: url(assets/images/author.png);
  background-repeat: no-repeat;
  background-position: center bottom;
}

</style>
