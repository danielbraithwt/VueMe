<template>
<div>
<card :always-expanded="false" :image="project.image">
  <h1 slot="top" class="Card-title">{{ project.name }}</h1>
  <p slot="top" class="Card-subtitle">{{ project.subtitle }}<p>

  <p slot="bottom">{{ project.description }}</p>

  <a slot="actions" class="Card-action Card-action--primary Ripple" v-bind:href="project.url">Explore</a>
  <a slot="actions" class="Card-action Ripple" v-bind:href="project.git">Source</a>
</card>
</div>
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
