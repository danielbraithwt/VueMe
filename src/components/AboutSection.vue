<template>
<div class="Fill--height">
  <div class="Container">
    <div class="row">
      <card :image="about.aboutme.image">
        <h1 slot="top">About Me</h1>
        <p slot="bottom">{{ about.aboutme.text }}</p>
      </card>


      <card :image="about.experence.image">
        <h1 slot="top">Experence</h1>
        <p slot="bottom">{{ about.experence.text }}</p>
        <div slot="bottom" class="Skills row">
          <skill v-for="skill in about.experence.skills"
                  :name="skill.name" :color="skill.color"></skill>
        </div>
      </card>

      <card :image="about.quallifications.image">
        <h1 slot="top">Quallifications</h1>
        <p slot="bottom">{{ about.quallifications.text }}</p>
      </card>
    </div>
  </div>
</div>
</template>

<script>
import Card from './Card.vue'
import Skill from './Skill.vue';

export default {
  name: 'about-section',
  props: ['about'],
  components: {
    Skill,
    Card
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

/*@media (min-wdith: 767px) {.u-sm-mh-0 {
  background-color: green;
  min-height: 0px !important;
}}*/
</style>
