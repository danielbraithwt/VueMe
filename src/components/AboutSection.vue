<template>
<div class="Fill--height">
  <div class="Container">
    <div class="row">
      <info-card :icon="about.aboutme.icon">
        <p slot="main">{{ about.aboutme.text }}</p>
      </info-card>


      <info-card :icon="about.experence.icon">
        <p slot="main">{{ about.experence.text }}</p>
        <div slot="bottom" class="Skills row">
          <skill v-for="skill in about.experence.skills"
                  :name="skill.name" :color="skill.color"></skill>
        </div>
      </info-card>

      <info-card :icon="about.quallifications.icon">
        <p slot="main">{{ about.quallifications.text }}</p>
      </info-card>
    </div>
  </div>
</div>
</template>

<script>
import InfoCard from './InfoCard.vue'
import Skill from './Skill.vue';

export default {
  name: 'about-section',
  props: ['about'],
  components: {
    Skill,
    InfoCard
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
