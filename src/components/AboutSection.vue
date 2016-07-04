<template>
<div class="Container">
  <div class="row">
    <div class="col-xs-12">
      <h1>Experence</h1>
    </div>
    <div class="col-xs-12 col-sm-6">
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    </div>
    <div class="col-xs-12 col-sm-6">
      <div class="Skills row">
        <skill></skill>
        <skill></skill>
        <skill></skill>
      </div>
    </div>
  </div>
</div>
</template>

<script>
import Skill from './Skill.vue';

export default {
  name: 'about-section',
  components: {
    Skill
  }
}
</script>

<style>
.Skills {
  display: flex;
  flex-wrap: wrap;
}
</style>
