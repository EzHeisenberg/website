<template>
  <div class="home">
    <Hero></Hero>
    <Paragraphe></Paragraphe>
    <Biographie></Biographie>
    <Skills></Skills>
    <Projets></Projets>
    <Footer></Footer>
  </div>
</template>

<script>
import Hero from "@/components/Home/Hero";
import Paragraphe from "@/components/Home/Paragraphe";
import Biographie from "@/components/Home/Biographie";
import Skills from "@/components/Home/Skills";
import Projets from "@/components/Home/Projets";
import Footer from "@/components/Footer";


export default {
  name: 'Home',
  components: {
    Hero,Paragraphe,Biographie,Skills,Projets,Footer
  }
}
</script>
