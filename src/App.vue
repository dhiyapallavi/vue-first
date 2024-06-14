<template>
  
  <div id="app">
    <nav-bar/>
    <home-bar/>
    <about-bar/>
    <about-us/>
    <count-section/>
    <service-section/>
    <more-section/>
    <feature-section/>
    <contact-section/>
    <footer-section/>
    </div>
    
</template>

<script>
import NavBar from './components/NavBar'
import HomeBar from './components/HomeBar.vue';
import AboutBar from './components/AboutBar.vue';
import AboutUs from './components/AboutUs.vue'
import CountSection from './components/CountSection.vue';
import ServiceSection from './components/ServiceSection.vue'
import MoreSection from './components/MoreSection.vue';
import FeatureSection from './components/FeatureSection.vue';
import ContactSection from './components/ContactSection.vue';
import FooterSection from './components/FooterSection.vue';


export default {
  name: 'App',
  components: {
    NavBar,
    HomeBar,
    AboutBar,
    AboutUs,
    CountSection,
    ServiceSection,
    MoreSection,
    FeatureSection,
    ContactSection,
    FooterSection
  }
}
</script>

<style>

</style>
