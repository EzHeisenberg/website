<template>
  <div class="hero">
    <div class="diagonal-hero-bg">
      <div class="hero-text">
        <h1 class="title">Lucas Reteau</h1>
        <p class="subtitle">Web Developer - Student</p>
      </div>
    </div>
    <img src="../../assets/avatar.png" alt="photo avatar" class="avatar">
  </div>
</template>

<script>
export default {
  name: "Hero"
}
</script>

<style lang="sass" scoped>

.avatar
  position: absolute
  width: 190px
  height: 190px
  margin: 0 auto
  top: 210px
  left: 0
  right: 0
  transition: all 1.2s ease-in-out


@media screen and (max-width: 570px)
  .avatar
    height: 130px
    width: 130px
    top: 240px

</style>