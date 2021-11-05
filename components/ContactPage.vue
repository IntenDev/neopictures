<template>
  <div>
    <div class="main">
      <a href="/">ГЛАВНАЯ</a><br>
      <a href="/gallery">ГАЛЕРЕЯ</a><br>
      <a href="/words">СЛОВА</a><br>
      <a href="/contact" class="action">КОНТАКТ  &bull;</a>
    </div>
    <div class="author">
      НЕОКАРТИНЫ <span>АЛЕКСЕЯ АНИСИМОВА<sup>Ѓ</sup></span>
    </div>
    <div id="addres">
      neokartina@mail.ru
      <!--,<br>
  +7 916 471 7711-->
    </div>
    <img class="pechat" src="~/assets/images/pechat.png" width="25" height="22">
  </div>
</template>

<script>
export default {
  name: 'ContactPage'
}
</script>

<style scoped>
#addres {
  font-size: 24px;
  position: absolute;
  left: 370px;
  margin: 0px;
  padding-top: 0px;
  padding-right: 0px;
  padding-bottom: 0px;
  padding-left: 0px;
  color: #5f6066;
  top: 200px;
  text-align: center;
  line-height: 36px;
}
</style>
