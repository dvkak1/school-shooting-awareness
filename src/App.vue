<script setup>
  import Navbar from "./components/NavbarComponent.vue";
  import Hero from "./components/Hero.vue";
  import Research from "./components/ResearchOverview.vue";
  import Incident from "./components/Incidents.vue";
  import 'bootstrap-icons/font/bootstrap-icons.css';
</script>


<template>
  <Navbar />
  <main>
    <Hero />
    <Research />
    <Incident />
  </main>
</template>
