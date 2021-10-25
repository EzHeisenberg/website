<template>


  <footer class="container-wbg section footer">
    <div class="navigation-bar-social">
      <ul id="navbar-social" class="items-social">
        <li>
          <a id="github-social" href="https://github.com/EzHeisenberg" target="_blank">
            <img alt="Icon GitHub" src="../assets/SocialNavigation/github.png">
          </a>
        </li>
        <li>
          <a id="linkedin-social" href="https://www.linkedin.com/in/lucas-reteau/" target="_blank">
            <img alt="Icon LinkedIn" src="../assets/SocialNavigation/linkedin.png">
          </a>
        </li>
        <li>
          <a id="instagram-social" href="https://www.instagram.com/heisen_dev/" target="_blank">
            <img alt="Icon Instagram" src="../assets/SocialNavigation/instagram.png">
          </a>
        </li>
        <li>
          <a id="mail-social" href="mailto:reteau.lucas-pro@outlook.fr">
            <img alt="Icon Mail" src="../assets/SocialNavigation/mail.png">
          </a>
        </li>
        <li>
          <a id="cv-social" href="">
            <img alt="Icon CV" src="../assets/SocialNavigation/cv.png">
          </a>
        </li>
      </ul>
    </div>
    <div class="logo-ez">
      <img alt="" src="../assets/favicon-night.png" width="40">
    </div>
    <div class="footer-navigation">
      <ul>
        <li><a class="link-style-2" href="">À propos de moi</a></li>
      </ul>
    </div>
    <p class="center copyright">© 2021 <a class="link-style-2" href="">EzForeach</a></p>
  </footer>
</template>


<script>

export default {
  name: "Footer",

}
</script>
<style lang="sass" scoped>

.link-style-contact
  padding: 15px 30px
  border: #ffb6fc 2px solid
  border-radius: 15px
  color: #fff
  transition: 0.2s ease-in

  &:hover
    color: #000
    background: #ffb6fc


.title-paragraphe
  padding: 0

.paragraphe
  padding: 0
  font-size: 16px

.columns
  display: grid
  grid-template-columns: 33.3% 33.3% 33.3%
  align-self: center


.column
  padding: 10px 20px

.contact
  padding: 10px 0
  border-radius: 20px
  margin: -7.5rem 7rem 1rem
  background: #1f1f1f
  text-align: center
  color: $light-background
  box-shadow: 6px 6px 18px 0 #3b3b3b

  div
    padding-bottom: 20px
    margin: auto auto


a.link-style-2
  color: white
  transition: 0.3s ease-in

  &:hover
    color: #1d1d1d


.footer-navigation
  font-family: $font-title-paragraphe
  text-align: center
  padding-bottom: 10px

  ul
    margin: auto
    padding: 10px 0
    list-style-type: none

    li
      display: inline
      padding: 0 20px


.navigation-bar-social
  ul
    width: fit-content
    margin: auto
    padding: 0
    list-style-type: none
    overflow: hidden

    li
      display: inline
      padding: 0 5px

      img
        height: calc(2vw + 30px)
        cursor: pointer
        padding: 5px


.container-wbg
  padding: 75px 0 10px

.copyright
  padding: 0 0 10px

.logo-ez
  padding: 5px
  display: flex
  justify-content: center


@media screen and (max-width: 1020px)
  .contact
    margin: -7.5rem 2rem 1rem

@media screen and (max-width: 820px)
  .columns
    display: grid
    grid-template-columns: auto
    align-self: center


@media screen and (max-width: 670px)

  .footer-navigation
    ul
      padding: 10px 0

      li
        padding: 0 5px
  .navigation-bar-social
    ul
      li
        img
          height: calc(2vw + 25px)


@media screen and (max-width: 500px)
  .navigation-bar-social
    ul
      li
        img
          height: calc(2vw + 20px)
  .footer-navigation
    ul
      li
        padding: 3px 5px
        display: block
</style>