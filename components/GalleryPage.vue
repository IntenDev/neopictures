<template>
  <div>
    <div class="main">
      <a href="/">ГЛАВНАЯ</a><br>
      <a href="/gallery" class="action">ГАЛЕРЕЯ &bull;</a><br>
      <a href="/words">СЛОВА</a><br>
      <a href="/contact">КОНТАКТ</a>
    </div>

    <div class="author">
      НЕОКАРТИНЫ <span>АЛЕКСЕЯ АНИСИМОВА<sup>Ѓ</sup></span>
    </div>
    <div class="main_wr">
      <a
        v-for="(pic, index) in currentCollection.pictures"
        :id="'img'+ (index + 1)"
        :key="index"
      >
        <img :src="require(`~/assets/images/collections/${currentCollection.folder}/${pic.min}`)" width="99" height="99" :class="{ action: isAction }" @click="selectPicture(index); makeAction()">
      </a>
    </div>
    <div class="gallery">
      <a :href="require(`~/assets/images/collections/${currentCollection.folder}/${picture.site}`)" target="_blank" class="centerIMG">
        <img :src="require(`~/assets/images/collections/${currentCollection.folder}/${picture.mod}`)" width="500" height="500">
      </a>
    </div>
    <div class="description">
      <em v-html="picture.description" />
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
      picture: data[0].pictures[0],
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
      this.picture = data[0].pictures[index]
    },
    makeAction () {
      this.isAction = true
    }
  }
}

</script>

<style scoped>

</style>
