
<template>
  <div class="section">
    <Header />
    <main>
      <div>
        <nuxt />
      </div>
    </main>
  </div>
</template>

<script>
import Header from '@/components/Header'
export default {
  name: 'Default',
  components: {
    Header
  }
}
</script>

<style scoped>

</style>
