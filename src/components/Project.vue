<template>
  <div class="col-xs-12 col-sm-6 col-md-4">
    <div class="Project Card">
      <div class="u-flex u-flexRow u-flexWrap">
        <div class="col-xs-12 u-p-0">
          <img class="Project-image" v-bind:src="project.image" />
        </div>

        <div class="Project-name col-xs-12 u-p-0">
          <h1>{{ project.name }}</h1>
        </div>

        <div class="Project-link col-xs-12 u-p-0">
          <img class="Project-link-icon" src="../../static/browser.svg" /> <a class="Project-link-text" v-bind:href="project.url">{{ project.url }}</a>
        </div>

        <div class="Project-link col-xs-12 u-mB-lg u-p-0">
          <img class="Project-link-icon" src="../../static/mark-github.svg" /> <a class="Project-link-text" v-bind:href="project.git">{{ project.git }}</a>
        </div>

        <div v-bind:class="{ 'Project-description--show':expanded }" class="Project-description col-xs-12 u-p-0">
          <p>{{ project.description }}</p>
        </div>

        <div class="col-xs-12 center-xs u-flex u-p-0 u-sm-hidden">
          <div v-on:click="toggleExpanded" v-bind:class="{ 'Projefct-expand--expanded':expanded }" class="Project-expand">
            <img src="../../static/chevron-down.svg" />
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
  props: ['project'],
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
