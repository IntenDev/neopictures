<template>
  <div class="container">
    <div class="row">
      <div class="main_wr col">
        <a
          v-for="(pic, index) in currentCollection.pictures"
          :id="'img'+ (index + 1)"
          :key="index"
        >
          <img :src="require(`~/assets/images/collections/${currentCollection.folder}/${pic.min}`)" width="99" height="99" :class="{ active: picture === pic }" @click="picture = pic">
        </a>
      </div>
      <div class="gallery col">
        <a :href="require(`~/assets/images/collections/${currentCollection.folder}/${picture.site}`)" target="_blank" class="centerIMG">
          <img :src="require(`~/assets/images/collections/${currentCollection.folder}/${picture.mod}`)" alt="">
        </a>
      </div>
      <div class="col">
        <div class="description">
          <!-- eslint-disable vue/no-v-html -->
          <em v-html="picture.description" />
        </div>
        <div class="caption">
          {{ currentCollection.name }},<br>
          {{ currentCollection.specific }},<br>
          {{ currentCollection.technology }}.
        </div>
      </div>

      <img class="pechat" src="~/assets/images/pechat.png" width="25" height="22" alt="Печать">
    </div>
  </div>
</template>

<script>
import data from '~/assets/json/data.json'
export default {
  name: 'GalleryPage',
  data () {
    return {
      picture: null
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
  created () {
    this.picture = this.currentCollection.pictures[0]
  }
}

</script>

<style scoped>

</style>
