<template>
  <section class="section container">
    <p class="title-paragraphe">Projets à l'affiche</p>
    <div class="content-wrapper">
      <div class="card-project">
        <router-link to="/project/0" class="card-project-link"></router-link>
        <img src="../../assets/Projects/mjp-portfolio.jpg" alt="" class="card-project-image">
        <div class="card-project-text-wrapper">
          <h2 class="card-project-title">Portfolio photographe</h2>
          <div class="card-project-date">10 juin, 2021</div>
          <div class="card-project-details">
            <p class="card-project-excerpt">
              Création d'un portfolio pour une photographe passionée.
            </p>
            <a href="#" class="card-project-more">Afficher plus</a>
          </div>
        </div>
      </div>


      <div class="card-project">
        <router-link to="/project/1" class="card-project-link"></router-link>
        <img src="../../assets/Projects/STPC/STPC.png" alt="" class="card-project-image">
        <div class="card-project-text-wrapper">
          <h2 class="card-project-title">ShopTitans Profit Calculator</h2>
          <div class="card-project-date">20 février, 2019</div>
          <div class="card-project-details">
            <p class="card-project-excerpt">
              Calculateur de bénéfice sur le jeu mobile "Shop Titans". Il permet de voir le gain d’expérience et le nombre de matériaux à utiliser.              </p>
            <a href="#" class="card-project-more">Afficher plus</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Projets"
}
</script>

<style lang="sass" scoped>

.content-wrapper
  margin: 0 auto
  max-width: 1200px
  display: flex
  flex-flow: row wrap
  justify-content: center
  padding: 0.5rem

.card-project
  border: 0 solid aqua
  margin: 0.5rem
  position: relative
  height: $card-height-large-screen
  overflow: hidden
  border-radius: 0.5rem
  flex: 1
  min-width: 290px
  font-family: $font-paragraphe
  box-shadow: 0 0 1rem rgba(0, 0, 0, 0.5)
  -webkit-backface-visibility: hidden
  -moz-backface-visibility: hidden
  -webkit-transform: translate3d(0, 0, 0)
  -moz-transform: translate3d(0, 0, 0)
  &::before
    content: ''
    position: absolute
    top: 0
    left: 0
    width: 100%
    height: 100%
    background: rgba(0, 0, 0, 0) linear-gradient(to bottom, rgba(0, 0, 0, 0) 50%, rgba(0, 0, 0, 0.7) 80%)
    z-index: 0


  &-link
    position: absolute
    top: 0
    left: 0
    width: 100%
    height: 100%
    z-index: 1


  &-image
    width: 100%
    height: 100%
    display: block
    object-fit: cover
    transition: transform 3s ease
    -webkit-backface-visibility: hidden
    backface-visibility: hidden
    position: relative
    z-index: -1

  &-text-wrapper
    position: absolute
    bottom: 0
    padding-bottom: 1rem
    color: white
    width: 100%
    transition: background-color 1.5s ease

  &-title
    font-family: $font-title-paragraphe
    padding: 0 1rem
    transition: color 1s ease
    margin-bottom: .5rem

  &-date
    padding: 0 1rem
    font-size: .7rem
    margin-bottom: .5rem
    color: #CCC

  &-details
    padding: 0 1rem
    max-height: 0
    opacity: 0
    transition: max-height 1.5s ease, opacity 1s ease


  &:hover &-details
    max-height: $card-height-large-screen
    opacity: 1

  &:hover &-text-wrapper
    background-color: rgba(0, 0, 0, 0.6)

  &:hover &-title
    color: #ffffff

  &:hover &-image
    transform: scale(1.2)
    z-index: -1

  &-excerpt
    font-weight: 300

  &-more
    background: black
    color: #bbb
    display: block
    padding: 0.4rem 0.6rem
    border-radius: 0.3rem
    margin-top: 1rem
    border: 1px solid #444
    font-size: 0.8rem
    -webkit-backface-visibility: hidden
    backface-visibility: hidden
    text-decoration: none
    width: 7rem
    margin-left: auto
    position: relative
    z-index: 5
    transition: 300ms ease-in-out
    &:hover
      color: $bg-left-mid

</style>