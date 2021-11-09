<template>
  <div class="section container">
    <div class="row">
      <div class="col" />
      <div id="addres" class="col">
        neokartina@mail.ru
        <!--,<br>
  +7 916 471 7711-->
      </div>
      <div class="col">
        <img class="pechat" src="~/assets/images/pechat.png" width="25" height="22" alt="Печать">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContactPage'
}
</script>

<style scoped>
#addres {
  font-size: 2rem;
  color: #5f6066;
  top: 200px;
  text-align: center;
  line-height: 36px;
}
</style>
