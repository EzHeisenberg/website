<template>
  <section class="section skill" id="skills">
    <div class="box">
      <div class="columns center">
        <div class="column">
          <figure class="image-skill"><img src="../../assets/Skills/backend.png" alt="backend image"></figure>
          <h2 class="title-skill">Développement Back-end</h2>
          <p class="paragraphe-skill space">
            Imaginer & créer une solution back-office intuitive afin de répondre au cahier des charges ou
            des problématiques rencontrées.
          </p>
          <p class="title-list-skills">Langages utilisés :</p>
          <p class="paragraphe-skill">PHP, Symfony, MySQL, JavaScript</p>
          <p class="title-list-skills">Ce que j'utilise :</p>
          <ul class="list-skill paragraphe-skill">
            <li class="list-skill-item">PHP Storm</li>
            <li class="list-skill-item">VS code</li>
            <li class="list-skill-item">Postman</li>
            <li class="list-skill-item">GitHub</li>
            <li class="list-skill-item">GitLab</li>
          </ul>
        </div>
        <div class="column">
          <figure class="image-skill"><img src="../../assets/Skills/frontend.png" alt="Front-end image"></figure>
          <h2 class="title-skill">Développement Front-end</h2>
          <p class="paragraphe-skill space">
            Donner vie à une idée, créer une page web en partant de rien. Styliser & dynamiser avec
            différents éléments et animations. </p>
          <p class="title-list-skills">Langages utilisés :</p>
          <p class="paragraphe-skill">HTML, CSS, Twig, Sass, JavaScript, VueJs</p>
          <p class="title-list-skills">Ce que j'utilise :</p>
          <ul class="list-skill paragraphe-skill">
            <li class="list-skill-item ">Adobe XD</li>
            <li class="list-skill-item">PHP Storm</li>
            <li class="list-skill-item">WebStorm</li>
            <li class="list-skill-item">Atom</li>
            <li class="list-skill-item">Figma</li>
            <li class="list-skill-item">GitHub</li>
            <li class="list-skill-item">GitLib</li>
          </ul>
        </div>
        <div class="column">
          <figure class="image-skill"><img src="../../assets/Skills/school.png" alt="Student image"></figure>
          <h2 class="title-skill">Étudiant <a href="https://www.epsi.fr/programmes/bachelor-informatique/"
                                              class="link-style">B3</a></h2>
          <p class="paragraphe-skill space">
            Étudiant en ingénierie informatique. Passionné par le métier de développeur. Cours basés sur
            +20h, avec projet scolaire.
          </p>
          <p class="title-list-skills">Cours théorique : </p>
          <p class="paragraphe-skill">POO, Algorithmique, </p>
          <p class="title-list-skills">Technologies étudiées :</p>
          <ul class="list-skill paragraphe-skill">
            <li class="list-skill-item">HTML, CSS, JavaScript</li>
            <li class="list-skill-item">PHP, Symfony</li>
            <li class="list-skill-item">C, C++, C#</li>
            <li class="list-skill-item">SQL, NoSQL</li>
            <li class="list-skill-item">NodeJS, VueJS</li>
            <li class="list-skill-item">Linux, Bash</li>
            <li class="list-skill-item">Projets scolaires</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Skills"
}
</script>

<style lang="sass" scoped>

.skill
  margin: -14rem 60px 100px
  padding: 0

.box
  border-radius: 12px
  color: $dark-background
  background-color: white
  box-shadow: 0 5px 5px 0 rgb(233 240 243 / 50%), 0 0 0 1px #e6ecf8
  display: block
  position: relative
  margin: 0 auto


.columns
  display: grid
  grid-template-columns: 33.3% 33.3% 33.3%
  align-self: center

.column
  border-right: 1px solid #dedede
  padding: 5px 20px

.column:last-child
  border-right: 0

.image-skill > img
  padding: 10px 0
  height: 90px
  width: 90px


.title-skill
  font-family: $font-title-paragraphe
  font-size: $size-title-paragraphe - 30px
  padding-bottom: 15px


.paragraphe-skill
  font-family: $font-paragraphe
  line-height: 29px
  font-size: 15px


.title-list-skills
  font-family: $font-title-paragraphe
  font-size: $size-title-paragraphe - 100px
  letter-spacing: 0.5px
  font-weight: 200
  color: $bg-left-mid
  padding: 35px 0 10px

.list-skill
  list-style: none
  margin: 0
  padding: 0 0 50px

.list-skill-item
  font-style: normal
  font-weight: 300



@media screen and (max-width: 820px)
  .columns
    display: block

  .column
    border-right: 0
    border-bottom: 1px solid #dedede

  .column:last-child
    border-bottom: 0


@media screen and (max-width: 670px)
  .skill
    margin: -14rem 40px 100px


@media screen and (max-width: 420px)
  .skill
    margin: -14rem 30px 100px
</style>