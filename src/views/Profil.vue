<template>
  <div class="Profil">
    <div class="image-profil">
      <img src="../assets/Profil/profil.jpg" alt="photo de profil">
    </div>
    <div class="content">
      <h1 class="title">Lucas Reteau</h1>


    </div>
  </div>
</template>

<script>
export default {
  name: "Profil"
}
</script>

<style lang="sass" scoped>

.Profil
  display: grid
  grid-template-columns: auto auto

.image-profil
  img
    position: absolute
    height: 100vh
    clip-path: polygon(0 0, 100% 0, 90% 25%, 100% 50%, 90% 75%, 100% 100%, 0 100%)

.content
  height: 100vh
  overflow: scroll




</style>