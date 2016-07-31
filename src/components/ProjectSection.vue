<template>

<div class="u-background">
  <div class="Container">
    <div class="MasonryColumn MasonryColumn--balanced">
      <template v-for="project in projects">
        <project class="col-xs-12 MasonryColumn-Item" :project="project"></project>
      </template>
    </div>
  </div>
</div>
</template>

<script>
import Project from './Project.vue';

export default {
  name: 'project-section',
  props: ['projects'],
  components: {
    Project
  }
}
</script>

<style>
</style>
