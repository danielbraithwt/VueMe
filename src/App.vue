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
  height: 100%;
  width: 100%;
}

.Fill--height {
  min-height: 100vh;
}

.Fill--width {
  width: 100%;
}

.Container {
  max-width: 96%;
  margin-left: 2%;
  margin-right: 2%;
}

.u-background {
  width: 100%;
  height: 100%;
  position: absolute;
  left: 0;
  top: 0;
  z-index: -2;

  background-color: #2196F3;
}
</style>
