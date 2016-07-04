<template>
  <div id="app">
    <header-section></header-section>
    <about-section></about-section>
    <project-section></project-section>
  </div>
</template>

<script>
import HeaderSection from './components/HeaderSection.vue';
import AboutSection from './components/AboutSection.vue';
import ProjectSection from './components/ProjectSection.vue';

export default {
  name: 'app',
  components: {
    HeaderSection,
    AboutSection,
    ProjectSection
  }
}
</script>

<style>
.Fill {
  min-height: 100vh;
}

.Container {
  max-width: 96%;
  margin-left: 2%;
  margin-right: 2%;
}

.h1--responsive {
  font-size: 5vw;
}

.p {

}
</style>
