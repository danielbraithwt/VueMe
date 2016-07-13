<template>
<div class="Container Fill--height">
  <div class="row">
    <div class="col-xs-12 u-flex u-flexJustifyContentCenter">
      <h1 class="Section-header u-title">About Me</h1>
    </div>
    <div class="col-xs-12">
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    </div>

    <div class="col-xs-12 u-flex u-flexJustifyContentCenter">
      <h1 class="Section-header u-title">Experence</h1>
    </div>
    <div class="col-xs-12">
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    </div>
    <div class="col-xs-12">
      <div class="Skills row">
        <skill name="JS" color="yellow"></skill>
        <skill name="Ember" color="amber"></skill>
        <skill name="Java" color="red"></skill>
        <skill name="Git" color="brown"></skill>
        <skill name="SASS" color="pink"></skill>
        <skill name="Vue" color="green"></skill>
      </div>
    </div>

    <div class="col-xs-12 u-flex u-flexJustifyContentCenter">
      <h1 class="Section-header u-title">Quallifications</h1>
    </div>
    <div class="col-xs-12">
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
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

.Section-header {
  margin-bottom: 0;
}
</style>
