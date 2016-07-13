<template>

<div class="Fill--height u-background">
  <div class="Container">
    <div class="row">
      <div class="col-xs-12 u-flex u-flexJustifyContentCenter">
        <h1 class="u-title u-textWhite">Projects</h1>
      </div>

      <div class="col-xs-12">
        <project></project>
        <project></project>
        <project></project>
      </div>
    </div>
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
