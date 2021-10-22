<template>
  <div id="app">
      <Navigation></Navigation>
      <router-view/>
  </div>
</template>

<script>
// @ is an alias to /src
import Navigation from '@/components/Navigation.vue'

export default {
  components: {
    Navigation,
  }
}
</script>



<style lang="sass">
@import "styles/variables.sass"


@font-face
  font-family: "BebasNeue"
  src: url("styles/fonts/BebasNeue-Regular.ttf") format("truetype")

@font-face
  font-family: "Pr"
  src: url("styles/fonts/Pr.ttf") format("truetype")

@font-face
  font-family: "eurostyleB"
  src: url("styles/fonts/EurostyleB.ttf") format("truetype")

@font-face
  font-family: "Europa"
  src: url("styles/fonts/mk2.ttf") format("truetype")


body
  margin: 0
  padding: 0
  min-height: 100vh
  .night-mode
      background: #2a2828
      color: white

.container
  padding: 0 10px

.container-wbg
  padding: 50px 10px 0
  color: $light-background
  background: #40769b  /* fallback for old browsers */
  background: $backgroun-gradiant-webkit
  background: $backgroun-gradiant
  filter: drop-shadow(0px 10px 5px rgba(0,0,0,0.4))

.section
  padding: 0 30px 100px

.narrow
  max-width: 2000px

.center
  text-align: center

.title
  font-family: $font-title
  letter-spacing: 5px
  text-align: center
  margin: 0
  padding-top: 20px
  font-size: $size-title
  -webkit-animation: title 1s cubic-bezier(0.215, 0.610, 0.355, 1.000) both
  animation: title 1s cubic-bezier(0.215, 0.610, 0.355, 1.000) both

.subtitle
  font-family: $font-subtitle
  letter-spacing: 0.5px
  font-size: $size-subtitle

.title-paragraphe
  padding: 50px 0
  font-family: $font-title-paragraphe
  font-size: $size-title-paragraphe
  letter-spacing: 1px
  text-align: center

.paragraphe
  font-family: $font-paragraphe
  font-size: $size-paragraphe
  font-style: normal
  line-height: 28px
  font-weight: 300
  max-width: 850px
  margin: auto

.transition-fade
  transition: 0.4s
  opacity: 1

html.is-animating .transition-fade
  opacity: 0

p
  margin: 0
  font-family: $font-paragraphe
  font-style: normal
  font-weight: 300
  font-size: $size-paragraphe

a
  text-decoration: none


a.link-style
  color: #ffb6fc
  transition: 0.2s ease-in
  &:hover
    color: #80a0ff



.hero
  display: inline-block
  width: 100%
  height: 360px
  position: relative
  z-index: -1
  filter: drop-shadow(0px 10px 5px rgba(0, 0, 0, 0.4))

.diagonal-hero-bg
  position: absolute
  top: 0
  left: 0
  width: 100%
  height: 350px
  z-index: -1
  background: #40769b
  background: $backgroun-gradiant-webkit
  background: $backgroun-gradiant
  clip-path: polygon(0 0, 100% 0, 100% 100%, 0 80%)

.hero-text
  padding-top: 60px
  text-align: center
  color: $light-background





/*

/*  IPAD - 1024x768  */
/*  IPAD PRO - 1366x1024  */
/*  IPHONE X - 375x812  */
/*  Galaxy S5 - 360x640  */
/*  Pixel XL 2 - 411x823  */



  @media screen and (max-width: 1020px)
  @media screen and (max-width: 820px)
  @media screen and (max-width: 670px)
  @media screen and (max-width: 570px)
  @media screen and (max-width: 420px)
  @media screen and (max-width: 375px)
  */


@media screen and (max-width: 670px)
  $size-title: 34px
  $size-paragraphe: 15px
  .title
    font-size: $size-title

  .paragraphe
    font-size: $size-paragraphe



@media screen and (max-width: 570px)



@media screen and (min-width: 500px)
  body
    &.light
      background-color: $light-background
      color: $dark-background
      transition: all 300ms ease-out
    &.dark
      background-color: $dark-background
      color: $light-background
      transition: all 300ms ease-out

















</style>
