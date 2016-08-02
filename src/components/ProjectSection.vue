<template>

<div class="u-background">
  <div class="Container">
    <div class="row">
      <div class="col-xs-12 center-xs">
        <h1 class="Title u-textWhite">Projects!</h1>
      </div>
    </div>
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
