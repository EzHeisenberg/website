<template>
  <div>
    <div class="hero">
      <div class="diagonal-hero-bg">
        <div class="hero-text">
          <h1 class="title">{{ title }}</h1>
        </div>
      </div>
    </div>

    <div class="container">
      <div class="grid-project">
        <div>
          <div class="slideshow-container">

            <div class="mySlides" v-for="(image, i) in pathImage" :key="i">
              <div class="numbertext paragraphe">{{ i + 1 }} / {{ pathImage.length }}</div>
              <img :src="require(`@/assets/Projects/${image}`)">
              <div class="text">{{ description }}</div>
            </div>

            <a class="prev" @click="plusSlides(-1)">&#10094;</a>
            <a class="next" @click="plusSlides(1)">&#10095;</a>

          </div>
          <div style="text-align:center">
            <span class="dotSlide" v-for="(i,j) in pathImage" :key="i" @click="currentSlide(j)"></span>
          </div>
        </div>

        <div>
          <div>
            <p class="title-paragraphe">Langage</p>
            <div class="grid-langage">
              <p class="paragraphe" v-bind:key="index" v-for="(item, index) in language">{{ item }}</p>
            </div>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>


<script>
import Projets from "@/files/Projets";


export default {
  name: "Project",
  data() {
    return {
      id: this.$route.params.id,
      title: "",
      description: "",
      language: [],
      url: "",
      pathImage: "",
      slideIndex: 1
    }
  },
  components: {},
  methods: {
    getProjet(index) {
      const projet = Projets.projets[index];
      this.title = projet.title;
      this.description = projet.description;
      this.language = projet.language;
      this.url = projet.url;
      this.pathImage = projet.pathImage;
    },


    showSlide(n) {
      let slides = document.getElementsByClassName('mySlides')
      let dotSlide = document.getElementsByClassName("dotSlide");

      if (n > slides.length) {
        this.slideIndex = 1
      }
      if (n < 1) {
        this.slideIndex = slides.length
      }
      for (let i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";
        dotSlide[i].className = dotSlide[i].className.replace(" active", "");
      }
      slides[this.slideIndex - 1].style.display = "block";
      dotSlide[this.slideIndex - 1].className += " active";


    },
    currentSlide(n) {
      this.slideIndex = n + 1
      this.showSlide(this.slideIndex);
    },
    plusSlides(n) {
      this.showSlide(this.slideIndex += n);
    },


  },
  created: function () {
    this.getProjet(this.id)
  },
  mounted: function () {
    this.showSlide(this.slideIndex)
  }
}
</script>


<style lang="sass" scoped>

*
  box-sizing: border-box

/* Slideshow container

.slideshow-container
  position: relative
  margin: auto


/* Hide the images by default

.mySlides
  display: none

  img
    height: auto
    width: 100%
    border-radius: 10px


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

/* Position the "next button" to the right

/* On hover, add a black background color with a little bit see-through

.prev:hover, .next:hover
  background-color: rgba(0, 0, 0, 0.6)

/* Caption text

.text
  color: #f2f2f2
  font-size: 15px
  padding: 8px 12px
  position: absolute
  bottom: 8px
  width: 100%
  text-align: center

/* Number text (1/3 etc)

.numbertext
  color: #f2f2f2
  padding: 8px 12px
  position: absolute
  top: 0

/* The dots/bullets/indicators

.dotSlide
  cursor: pointer
  height: 10px
  width: 10px
  margin: 0 2px
  background-color: #dcdcdc
  border-radius: 50%
  display: inline-block
  transition: background-color 0.6s ease

.active, .dotSlide:hover
  background-color: #e69eee

/* Fading animation

.fade
  -webkit-animation-name: fade
  -webkit-animation-duration: 1.5s
  animation-name: fade
  animation-duration: 1.5s

@-webkit-keyframes fade
  from
    opacity: .4

  to
    opacity: 1

@keyframes fade
  from
    opacity: .4

  to
    opacity: 1


.diagonal-hero-bg
  height: 230px

.hero
  height: 260px

.title-paragraphe
  padding: 15px 0

.grid-langage
  display: grid
  grid-template-columns: auto auto auto auto
  text-align: center
  justify-content: center
  grid-gap: 5px

.grid-project
  display: grid
  grid-template-columns: 55% 35%
  justify-content: space-around


@media screen and (max-width: 860px)
  .grid-project
    display: grid
    grid-template-columns: auto

@media screen and (max-width: 630px)
  .title
    font-size: 2rem

</style>