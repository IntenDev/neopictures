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
      <a
        v-for="(picture, index) in currentCollection.pictures"
        :id="'img'+ (index + 1)"
        :key="index"
      >
        <img :src="require(`~/assets/images/collections/${currentCollection.folder}/${picture.min}`)" width="99" height="99" :class="{ action: isAction }" @click="selectPicture(index); makeAction()">
      </a>
    </div>
    <div class="gallery">
      <a :href="require(`~/assets/images/collections/${currentCollection.folder}/${pictureSite}`)" target="_blank" class="centerIMG">
        <img :src="require(`~/assets/images/collections/${currentCollection.folder}/${pictureBig}`)" width="500" height="500">
      </a>
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
  data () {
    return {
      collections: data,
      pictureBig: data[0].pictures[0].mod,
      pictureSite: data[0].pictures[0].site,
      isAction: false
    }
  },
  computed: {
    collectionData () {
      return data
    },
    currentCollection () {
      return this.collectionData[0]
    }
  },
  methods: {
    selectPicture (index) {
      this.pictureBig = data[0].pictures[index].mod
    },
    makeAction () {
      this.isAction = true
    }
  }
}

</script>

<style scoped>

</style>
