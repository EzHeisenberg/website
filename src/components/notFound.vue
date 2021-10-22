<template>
  <div>
    <div class="banner"></div>
    <div class="container">
      <h2 class="title"><span>404</span> Found</h2>
      <p class="paragraphe center">Nous sommes désolés pour cet inconvenient.</p>
      <p class="paragraphe center">Un problème est survenu, la page que vous cherchez est indisponible</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "notFound"
}
</script>

<style lang="sass" scoped>
.title
  span
    font-size: 76px

.banner
  height: 221px
  background: $bg-left
  background: $backgroun-gradiant-webkit
  background: $backgroun-gradiant


</style>