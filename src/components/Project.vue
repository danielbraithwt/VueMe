<template>
<card :image="project.image">
  <h1 slot="top" class="Project-name">{{ project.name }}</h1>
  <div slot="top" class="Project-link col-xs-12 u-p-0">
    <img class="Project-link-icon" src="../../static/browser.svg" /> <a class="Project-link-text" v-bind:href="project.url">{{ project.url }}</a>
  </div>
  <div slot="top" class="Project-link col-xs-12 u-mB-lg u-p-0">
    <img class="Project-link-icon" src="../../static/mark-github.svg" /> <a class="Project-link-text" v-bind:href="project.git">{{ project.git }}</a>
  </div>

  <p slot="bottom">{{ project.description }}</p>
</card>
</template>

<script>
import Card from './Card.vue';
import Skill from './Skill.vue';

export default {
  name: 'project',
  props: ['project'],
  components: [
    Skill,
    Card
  ],
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
</style>
