<template>
  <NavBar/>
  <HeroSection/>
  <JohnLegend/>
  <MuzeheSection/>
  <CarouselSection/>
  <FooterSection/>
</template>

<script>
import NavBar from './components/NavBar.vue';
import CarouselSection from './components/CarouselSection.vue'
import HeroSection from './components/HeroSection.vue'
import JohnLegend from './components/JohnLegend.vue';
import MuzeheSection from './components/MuzeheSection.vue';
import FooterSection from './components/FooterSection.vue';

export default {
  name: 'App',
  components: {
    NavBar,
    HeroSection,
    JohnLegend,
    MuzeheSection,
    CarouselSection,
    FooterSection

  }
}
</script>

