<template>
  <div id="app">
    <header-section></header-section>
  </div>
</template>

<script>
import HeaderSection from './components/HeaderSection.vue';

export default {
  name: 'app',
  components: {
    HeaderSection
  }
}
</script>

<style>
.Fill {
  width: 100%;
  height: 100%;
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
