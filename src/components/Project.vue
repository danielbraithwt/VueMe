<template>
  <div class="col-xs-12 col-sm-6 col-md-4">
    <div class="Project">
      <div class="u-flex u-flexRow u-flexWrap">
        <div class="col-xs-12 u-p-0">
          <img class="Project-image" src="http://placehold.it/500x250" />
        </div>

        <div class="Project-name col-xs-12 u-p-0">
          <h1>Name</h1>
        </div>

        <!-- <div class="Project-skills col-xs-12">
          <skill name="Git" color="brown"></skill>
          <skill name="SASS" color="pink"></skill>
          <skill name="Vue" color="green"></skill>
        </div> -->

        <div class="Project-link col-xs-12 u-p-0">
          <img class="Project-link-icon" src="../assets/browser.svg" /> <a class="Project-link-text" href="#">http://www.website.com</a>
        </div>

        <div class="Project-link col-xs-12 u-mB-lg u-p-0">
          <img class="Project-link-icon" src="../assets/mark-github.svg" /> <a class="Project-link-text" href="#">https://github.com/danielbraithwt</a>
        </div>

        <div v-bind:class="{ 'Project-description--show':expanded }" class="Project-description col-xs-12 u-p-0">
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
        </div>

        <div class="col-xs-12 center-xs u-flex u-p-0 u-sm-hidden">
          <div v-on:click="toggleExpanded" v-bind:class="{ 'Projefct-expand--expanded':expanded }" class="Project-expand">
            <img src="../assets/chevron-down.svg" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Skill from './Skill.vue';

export default {
  name: 'project',
  components: [Skill],
  data: function() {
    return {
      expanded: false,
    };
  },
  methods: {
    toggleExpanded: function(event) {
      this.expanded = !this.expanded;
    }
  }
}
</script>

<style>
.Project {
  height: auto;

  padding-bottom: 20px;

  /*margin-top: 40px;*/
  margin-bottom: 40px;
  /*padding: 40px;*/

  box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);

  border-radius: 2px;

  background-color: white;
}

.Project-expand {
  width: 50px;
  height: 50px;

  margin-bottom: -40px;

  box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);

  border-radius: 50%;

  background-color: white;

  display: flex;
  justify-content: center;
}

.Project-expand img {
  transform: rotate(0deg);
  transition: transform 600ms cubic-bezier(0.645, 0.045, 0.355, 1);
}

.Projefct-expand--expanded img {
  transform: rotate(180deg);
}

.Project-image {
  width: 100%;
}

.Project-name {
  display: flex;
  justify-content: flex-start;
  align-items: center;

  /*color: white;*/

  padding-left: 20px;
}

.Project-name h1 {
  margin-bottom: 0;
}

.Project-link {
  display: flex;

  padding-top: 5px;
  padding-left: 20px;
}

.Project-link-icon {
  width: 24px;
  padding-right: 10px;
}

.Project-link-text {

}

.Project-skills {
  display: flex;
  padding-top: 10px;
}

.Project-description {
  max-height: 0px;
  overflow: hidden;
  transition: max-height 400ms cubic-bezier(0.645, 0.045, 0.355, 1);

  padding-left: 20px;
  padding-right: 20px;
}

.Project-description--show {
  max-height: 1000px;
}

@media (min-width: 767px) {.Project-description {
    max-height: 1000px;
}}
</style>
