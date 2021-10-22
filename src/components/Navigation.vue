<template>
  <div>
    <svg>
      <defs>
        <filter id="gooeyness">
          <feGaussianBlur in="SourceGraphic" stdDeviation="2.2" result="blur"/>
          <feColorMatrix in="blur" mode="matrix" values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 20 -10"
                         result="gooeyness"/>
          <feComposite in="SourceGraphic" in2="gooeyness" operator="atop"/>
        </filter>
      </defs>
    </svg>
    <div class="plates" id="burgerContainer">
      <div class="plate plate2" id="plate-toggle" v-on:click="toggleMenu">
        <svg class="burger" version="1.1" height="100" width="100" viewBox="0 0 100 100">
          <path class="line line1"
                d="M 50,65 H 70 C 70,65 75,65.198488 75,70.762712 C 75,73.779026 74.368822,78.389831 66.525424,78.389831 C 22.092231,78.389831 -18.644068,-30.508475 -18.644068,-30.508475"/>
          <path class="line line2"
                d="M 50,35 H 70 C 70,35 81.355932,35.300135 81.355932,25.635593 C 81.355932,20.906215 78.841706,14.830508 72.881356,14.830508 C 35.648232,14.830508 -30.508475,84.322034 -30.508475,84.322034"/>
          <path class="line line3"
                d="M 50,50 H 30 C 30,50 12.288136,47.749959 12.288136,60.169492 C 12.288136,67.738339 16.712974,73.305085 40.677966,73.305085 C 73.791674,73.305085 108.47458,-19.915254 108.47458,-19.915254"/>
          <path class="line line4"
                d="M 50,50 H 70 C 70,50 81.779661,50.277128 81.779661,36.607372 C 81.779661,28.952694 77.941689,25 69.067797,25 C 39.95532,25 -16.949153,119.91525 -16.949153,119.91525"/>
          <path class="line line5"
                d="M 50,65 H 30 C 30,65 17.79661,64.618439 17.79661,74.152543 C 17.79661,80.667556 25.093813,81.355932 38.559322,81.355932 C 89.504001,81.355932 135.59322,-21.186441 135.59322,-21.186441"/>
          <path class="line line6"
                d="M 50,35 H 30 C 30,35 16.525424,35.528154 16.525424,24.152542 C 16.525424,17.535987 22.597755,13.559322 39.40678,13.559322 C 80.617882,13.559322 94.067797,111.01695 94.067797,111.01695"/>
        </svg>
        <svg class="x" version="1.1" height="100" width="100" viewBox="0 0 100 100">
          <path class="line" d="M 34,32 L 66,68"/>
          <path class="line" d="M 66,32 L 34,68"/>
        </svg>
      </div>
    </div>
    <div id="sidenavMenu" class="sidenav">
      <div class="cards-list">
        <router-link to="/">
          <div class="card" v-on:click="toggleMenu">
            <img class="card_image" src="../assets/Navigation/home.png" alt="icon accueil"/>
            <div class="card_title">
              Accueil
            </div>
          </div>
        </router-link>
        <router-link to="/portfolio">
          <div class="card" v-on:click="toggleMenu">
            <img class="card_image" src="../assets/Navigation/portfolio.png" alt="icon portfolio"/>
            <div class="card_title">
              Portfolio
            </div>
          </div>
        </router-link>
        <router-link to="/profil">
          <div class="card" v-on:click="toggleMenu">
            <img class="card_image" src="../assets/Navigation/profil.png" alt="icon profile"/>
            <div class="card_title">
              Profil
            </div>
          </div>
        </router-link>

        <a href="https://github.com/EzHeisenberg" target="_blank">
          <div class="card" v-on:click="toggleMenu">
            <img class="card_image" src="../assets/Navigation/github.png" alt="icon github"/>
            <div class="card_title">
              GitHub
            </div>
          </div>
        </a>
        <a href="https://www.linkedin.com/in/lucas-reteau/" target="_blank">
          <div class="card" v-on:click="toggleMenu">
            <img class="card_image" src="../assets/Navigation/linkedin.png" alt="icon linkedin"/>
            <div class="card_title">
              LinkedIn
            </div>
          </div>
        </a>
        <a href="https://instagram.com/heisen_dev/" target="_blank">
          <div class="card" v-on:click="toggleMenu">
            <img class="card_image" src="../assets/Navigation/instagram.png" alt="icon instagram"/>
            <div class="card_title">
              Instagram
            </div>
          </div>
        </a>
        <a href="https://discordapp.com/users/479704172128632832/" target="_blank">
          <div class="card" v-on:click="toggleMenu">
            <img class="card_image" src="../assets/Navigation/discord.png" target="_blank" alt="icon discord"/>
            <div class="card_title">
              Discord
            </div>
          </div>
        </a>
        <a href="https://open.spotify.com/playlist/41LOdawD3vUgmfWdw0srlx?si=8ziRCqIkRC6tOYlN6BVaDg" target="_blank">
          <div class="card" v-on:click="toggleMenu">
            <img class="card_image" src="../assets/Navigation/spotify.png" alt="icon spotify"/>
            <div class="card_title">
              Spotify
            </div>
          </div>
        </a>
        <router-link to="/calculator">
          <div class="card" v-on:click="toggleMenu">
            <img class="card_image" src="../assets/Navigation/calculator.png" alt="icon calculatrice"/>
            <div class="card_title">
              Calculatrice
            </div>
          </div>
        </router-link>
      </div>
      <div class="dock" id="dock">
        <div class="dots-dock" id="dots">
          <div class="dot"></div>
        </div>
        <div class="cards-dock">
          <a href="https://account.xbox.com/fr-fr/profile?gamertag=Ez%20Heisenberg" target="_blank">
            <div class="card" v-on:click="toggleMenu">
              <img class="card_image" src="../assets/Navigation/xbox.png" alt="icon xbox"/>
            </div>
          </a>
          <a href="https://www.facebook.com/lucas.reteau.75/" target="_blank">
            <div class="card" v-on:click="toggleMenu">
              <img class="card_image" src="../assets/Navigation/facebook.png" alt="icon facebook"/>
            </div>
          </a>
          <a href="">
            <div class="card" v-on:click="toggleMenu">
              <img class="card_image" src="../assets/Navigation/sms.png" alt="icon sms"/>
            </div>
          </a>
          <a href="mailto:reteau.lucas-pro@outlook.fr">
            <div class="card" v-on:click="toggleMenu">
              <img class="card_image" src="../assets/Navigation/mail.png" alt="icon mail"/>
            </div>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: "Navigation",
  data() {
    return {
      isActive: false
    }
  },
  methods: {
    toggleMenu: function () {
      this.isActive = !this.isActive;

      const sidenav = document.getElementById("sidenavMenu");
      const plates = document.getElementById("plate-toggle");
      let cards = document.getElementsByClassName("card");
      const dock = document.getElementById("dock");

      if (!this.isActive) {

        dock.classList.remove("dock-in");
        plates.classList.remove('active-burger');
        dock.classList.add("dock-out");

        for (let i = 0; i < cards.length; i++) {
          cards.item(i).classList.remove("card-in");
          cards.item(i).classList.add("card-out");
        }
        setTimeout(() => {
          sidenav.style.width = "0";
        }, 400);
      } else {
        dock.classList.remove("dock-out");
        dock.classList.add("dock-in");
        plates.classList.add('active-burger');

        for (let i = 0; i < cards.length; i++) {
          cards.item(i).classList.remove("card-out");
          cards.item(i).classList.add("card-in");
        }
        sidenav.style.width = "100%";
      }
    },
  }

}

</script>
<style lang="sass">

.sidenav
  height: 100%
  width: 0
  position: fixed
  top: 0
  left: 0
  background-image: url("../assets/Navigation/wallpaper.jpg")
  background-position: center
  background-repeat: no-repeat
  background-size: cover
  overflow-x: hidden
  transition: 0.5s
  text-align: center
  z-index: 10

.cards-list
  padding-top: 33px
  text-align: center
  width: calc(100% - 1px)
  margin: 0 auto
  display: grid
  grid-template-columns: auto auto auto auto auto auto

.dock
  position: absolute
  bottom: 30px
  left: 0
  right: 0
  .cards-dock
    text-align: center
    width: calc(100vw - 180px)
    background-color: rgba(214, 214, 214, 0.67)
    border-radius: 30px
    display: grid
    grid-template-columns: auto auto auto auto
    margin: auto

  .dots-dock
    .dot
      height: 8px
      width: 8px
      border-radius: 50%
      background-color: #8a8a8a
      margin: 5px auto

.card
  margin: 20px auto
  width: 95px
  height: 95px
  border-radius: 20px
  cursor: pointer
  text-decoration: none
  color: #111111
  transition: 0.3s ease-in

  &:hover
    .card_image
      box-shadow: 5px 5px 15px 10px rgba(0, 0, 0, 0.15), -5px -5px 15px 10px rgba(0, 0, 0, 0.12)
      transform: scale(0.9, 0.9)
    .card_title
      transform: scale(0.9, 0.9)

  .card_image
    width: inherit
    height: inherit
    border-radius: 20px
    transition: 0.3s ease-in

  .card_title
    text-align: center
    font-family: sans-serif
    padding: 5px
    font-size: 17px
    transition: 0.3s ease-in


svg
  height: 60px
  width: 60px
  position: fixed

.plates
  right: 0
  top: 0
  position: absolute
  cursor: pointer
  display: flex
  flex-wrap: wrap
  max-height: 60px
  width: fit-content

.plate
  height: 60px
  width: 60px
  z-index: 11

.burger
  filter: url(#gooeyness)
  z-index: 11

.x
  transform: scale(0)
  transition: transform 400ms

.line
  fill: none
  stroke: black
  stroke-width: 6.5px
  stroke-linecap: round
  stroke-linejoin: round
  transform-origin: 50%
  transition: stroke-dasharray 500ms 200ms, stroke-dashoffset 500ms 200ms, transform 500ms 200ms

.x .line
  stroke-width: 4.8px

.active-burger .x
  transform: scale(1)
  transition: transform 400ms 350ms

.plate2
  .line1
    stroke-dasharray: 21 185.62753295898438

  .line2
    stroke-dasharray: 21 178.6514129638672
    transition-delay: 30ms

  .line3
    stroke-dasharray: 21 197.92425537109375
    transition-delay: 60ms

  .line4
    stroke-dasharray: 21 190.6597137451172
    transition-delay: 90ms

  .line5
    stroke-dasharray: 21 208.52874755859375
    transition-delay: 120ms

  .line6
    stroke-dasharray: 21 186.59703063964844
    transition-delay: 150ms

.active-burger.plate2
  .line1
    stroke-dasharray: 5 185.62753295898438
    stroke-dashoffset: -141px

  .line2
    stroke-dasharray: 5 178.6514129638672
    stroke-dashoffset: -137px

  .line3
    stroke-dasharray: 5 197.92425537109375
    stroke-dashoffset: -176px

  .line4
    stroke-dasharray: 5 190.6597137451172
    stroke-dashoffset: -159px

  .line5
    stroke-dasharray: 5 208.52874755859375
    stroke-dashoffset: -139px

  .line6
    stroke-dasharray: 5 186.59703063964844
    stroke-dashoffset: -176px

  .x
    transition: transform 400ms 250ms


@media screen and (max-width: 820px)
  .cards-list
    grid-template-columns: auto auto auto auto auto

  .dock
    .cards-dock
      width: calc(100vw - 70px)

  .card
    height: 80px
    width: 80px
    .card_image
      width: inherit
      height: inherit
      border-radius: 20px
    .card_title
      font-size: 15px

@media screen and (max-width: 670px)
  .card
    .card_title
      font-size: 13px


@media screen and (max-width: 570px)
  .cards-list
    grid-template-columns: auto auto auto auto

  .dock
    .dots-dock
      .dot
        height: 6px
        width: 6px

    .cards-dock
      width: calc(100% - 50px)
      bottom: 10px
      .card
        width: 60px
        height: 60px
        border-radius: 15px
        .card_image
          width: inherit
          height: inherit
          border-radius: 15px

  .card
    width: 70px
    height: 70px
    border-radius: 15px
    .card_image
      width: inherit
      height: inherit
      border-radius: 15px
      img
        border-radius: 15px


@media screen and (max-width: 390px)
  .dock
    .cards-dock
      width: calc(100% - 15px)




@media screen and (max-height: 650px)
  .cards-dock
    display: none


</style>