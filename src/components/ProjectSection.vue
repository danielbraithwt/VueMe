<template>
<div class="Container">
  <div class="row">
    <h1 class="h1--responsives">Projects</h1>
  </div>
  <div class="row">
    <project></project>
    <project></project>
    <project></project>
  </div>
</div>
</template>

<script>
import Project from './Project.vue';

export default {
  name: 'project-section',
  components: {
    Project
  }
}
</script>

<style>

</style>
