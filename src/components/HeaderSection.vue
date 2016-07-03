<template>
  <div class="Container">
    <div class="row middle-xs">
      <div class="col-xs-12 col-sm-6 center-xs">
        <div class="box">
          <img src="https://placehold.it/150x150" />
          <h1 class="h1--responsive">Daniel Braithwaite</h1>
          <social></social>
        </div>
      </div>

      <div class="col-xs-12 col-sm-6 center-xs">
        <div class="box">
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Social from './Social.vue';

export default {
  name: 'header-section',
  components: {
    Social
  }
}
</script>

<style>

</style>
