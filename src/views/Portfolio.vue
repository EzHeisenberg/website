<template>
  <div class="Portfolio">
    <div class="hero">
      <div class="diagonal-hero-bg">
        <div class="hero-text">
          <h1 class="title">Portfolio</h1>
        </div>
      </div>
    </div>

    <div class="container">


      <div>
        <h3 class="title-paragraphe">Projets GITHUB</h3>

        <p v-if="errored" class="paragraphe">GitHub ne répond pas.</p>

        <div v-else>
          <div v-if="loading">Chargement...</div>


          <div class="card-container">

            <div class="projet-slide" v-for="(projet, i) in projetsGit" :key="i">
              <div class="paragraphe" id="name">{{ projet.name }}</div>
              <div class="paragraphe">{{ projet.private }}</div>
              <div class="paragraphe">{{ projet.created_at }}</div>
              <div class="paragraphe">{{ projet.updated_at }}</div>
              <div class="paragraphe">{{ projet.html_url }}</div>
              <div class="paragraphe">{{ projet.description }}</div>
              <div class="paragraphe">{{ projet.clone_url }}</div>
              <div class="paragraphe">{{ projet.stargazers_count }}</div>
              <div class="paragraphe">{{ contributorsGit }}</div>
            </div>

          </div>

          <a class="prev" @click="plusSlides(-1)">&#10094;</a>
          <a class="next" @click="plusSlides(1)">&#10095;</a>


        </div>

      </div>
    </div>


  </div>
</template>


<style lang="sass" scoped>


.diagonal-hero-bg
  height: 230px

.hero
  height: 260px
  margin-bottom: -60px


.card-container
  border: 1px solid black


/* Next & previous buttons

.prev
  cursor: pointer
  position: absolute
  top: 50%
  width: auto
  margin-top: -22px
  padding: 16px
  color: white
  font-weight: bold
  font-size: 18px
  transition: 0.6s ease
  border-radius: 0 3px 3px 0
  user-select: none

.next
  cursor: pointer
  position: absolute
  top: 50%
  width: auto
  margin-top: -22px
  padding: 16px
  color: white
  font-weight: bold
  font-size: 18px
  transition: 0.6s ease
  user-select: none
  right: 0
  border-radius: 3px 0 0 3px

.prev:hover, .next:hover
  background-color: rgba(0, 0, 0, 0.6)


@media screen and (max-width: 1020px)

@media screen and (max-width: 820px)

@media screen and (max-width: 670px)

@media screen and (max-width: 570px)

@media screen and (max-width: 420px)

@media screen and (max-width: 375px)

</style>

<script>

import axios from "axios";

export default {
  name: 'Portfolio',
  data() {
    return {
      projetsGit: [],
      contributorsGit: [],


      slideIndex: 1,


      loading: true,
      errored: false

    }
  },
  components: {},
  methods: {
    getAllRepoGit(){
      axios
          .get('https://api.github.com/users/EzHeisenberg/repos')
          .then(response => {
            this.projetsGit = response.data
          })
          .catch(error => {
            console.log(error)
            this.errored = true
          })
          .finally(() => {
            this.loading = false;
            this.showProjetGit(this.slideIndex)
          })
    },

    getContributorsRepo(name){
      axios
          .get(`https://api.github.com/repos/EzHeisenberg/${name}/contributors`)
          .then(response => {
            this.contributorsGit = response.data
          })
          .catch(error => {
            console.log(error)
          })
          .finally(() => {
            this.loading = false;
          })
    },

    showProjetGit(n) {
      let slides = document.getElementsByClassName('projet-slide')

      if (n > slides.length) {
        this.slideIndex = 1
      }
      if (n < 1) {
        this.slideIndex = slides.length
      }
      for (let i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";
      }
      slides[this.slideIndex - 1].style.display = "block";


      this.getContributorsRepo()
    },
    currentSlide(n) {
      this.slideIndex = n + 1
      this.showProjetGit(this.slideIndex);

      this.getContributorsRepo()


    },
    plusSlides(n) {
      this.showProjetGit(this.slideIndex += n);



    },


  },
  created: function () {

  },
  mounted: function () {
    this.getAllRepoGit()

  }
}
</script>
