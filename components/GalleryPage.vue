<template>
  <div>
    <div class="main">
      <NuxtLink to="/">
        ГЛАВНАЯ
      </NuxtLink>
      <br>
      <a href="/gallery" class="action">ГАЛЕРЕЯ &bull;</a><br>
      <a href="words.html">СЛОВА</a><br>
      <a href="contact.html">КОНТАКТ</a>
    </div>
    <div class="author">
      НЕОКАРТИНЫ <span>АЛЕКСЕЯ АНИСИМОВА<sup>Ѓ</sup></span>
    </div>
    <div class="main_wr">
      <a v-for="(picture, index) in currentCollection.pictures" :id="'img'+ (index + 1)" :key="index"><img :src="require(`~/assets/images/collections/${currentCollection.folder}/${picture.min}`)" width="99" height="99"></a>
    </div>
    <div class="gallery">
      <a href="~/assets/images/1-site.jpg" target="_blank" class="centerIMG"><img src="~/assets/images/collections/yunaya-ivolga/1-mod.jpg" width="500" height="500"></a>
    </div>
    <div class="description">
      <em>&hellip; Заблудилась<br>
        Юная Иволга<br>
        В небесных полях,<br>
        Ищет нас с тобою<br>
        Любимая,<br>
        Среди облаков &hellip;<br>
      </em>
    </div>
    <img class="pechat" src="~/assets/images/pechat.png" width="25" height="22">
    <div class="caption">
      {{ currentCollection.name }},<br>
      {{ currentCollection.specific }},<br>
      {{ currentCollection.technology }}.
    </div>
  </div>
</template>

<script>
import data from '~/assets/json/data.json'
export default {
  name: 'GalleryPage',
  computed: {
    collectionData () {
      return data
    },
    currentCollection () {
      return this.collectionData[0]
    }
  }
}

</script>

<style scoped>

</style>
