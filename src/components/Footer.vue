<template>


  <footer class="container-wbg section footer">
    <div class="columns center contact">
      <div class="column">
        <h2 class="title-paragraphe">Commencé un projet</h2>
      </div>
      <div class="column">
        <p class="paragraphe">Si vous voulez me confier votre projet, prenons contact, je payerais le café</p>
      </div>
      <div class="column">
        <a href="" class="link-style-contact">Contactez-moi</a>
      </div>
    </div>



    <div class="navigation-bar-social">
      <ul class="items-social" id="navbar-social">
        <li>
          <a href="https://github.com/EzHeisenberg" target="_blank" id="github-social">
            <img src="../assets/SocialNavigation/github.png" alt="Icon GitHub">
          </a>
        </li>
        <li>
          <a href="https://www.linkedin.com/in/lucas-reteau/" target="_blank" id="linkedin-social">
            <img src="../assets/SocialNavigation/linkedin.png" alt="Icon LinkedIn">
          </a>
        </li>
        <li>
          <a href="https://www.instagram.com/heisen_dev/" target="_blank" id="instagram-social">
            <img src="../assets/SocialNavigation/instagram.png" alt="Icon Instagram">
          </a>
        </li>
        <li>
          <a href="mailto:reteau.lucas-pro@outlook.fr" id="mail-social">
            <img src="../assets/SocialNavigation/mail.png" alt="Icon Mail">
          </a>
        </li>
        <li>
          <a href="" id="cv-social">
            <img src="../assets/SocialNavigation/cv.png" alt="Icon CV">
          </a>
        </li>
      </ul>
    </div>
    <div class="logo-ez">
      <img src="../assets/favicon-night.png" alt="" width="40">
    </div>
    <div class="footer-navigation">
      <ul>
        <li><a href="" class="link-style-2">À propos de moi</a></li>
        <li><a href="" class="link-style-2">Faire un devis</a></li>
        <li><a href="" class="link-style-2">Travailler ensemble</a></li>
      </ul>
    </div>
    <p class="center copyright">© 2021 <a href="" class="link-style-2">EzForeach</a></p>
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
  font-size: 15px

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