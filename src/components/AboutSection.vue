<template>
<div class="Fill--height">
  <div class="Container">
    <div class="row">
      <div class="col-xs-12 u-flex u-flexJustifyContentCenter">
        <h1>Me</h1>
      </div>
      <div class="col-xs-12 col-sm-6 col-md-4 u-flex">
        <div class="Card">
          <div class="col-xs-12 u-flex u-flexJustifyContentCenter">
            <h1 class="Section-header u-title">About Me</h1>
          </div>
          <div class="col-xs-12">
            <p>{{ about.aboutme }}</p>
          </div>
        </div>
      </div>

      <div class="col-xs-12 col-sm-6 col-md-4 u-flex">
        <div class="Card">
          <div class="col-xs-12 u-flex u-flexJustifyContentCenter">
            <h1 class="Section-header u-title">Experence</h1>
          </div>
          <div class="col-xs-12">
            <p>{{ about.experence.text }}</p>
          </div>
          <div class="col-xs-12">
            <div class="Skills row">
              <skill v-for="skill in about.experence.skills"
                      :name="skill.name" :color="skill.color"></skill>
            </div>
          </div>
        </div>
      </div>

      <div class="col-xs-12 col-sm-6 col-md-4 u-flex">
        <div class="Card">
          <div class="col-xs-12 u-flex u-flexJustifyContentCenter">
            <h1 class="Section-header u-title">Quallifications</h1>
          </div>
          <div class="col-xs-12">
            <p>{{ about.quallifications }}</p>
          </div>
        </div>

        </div>
    </div>
  </div>
</div>
</template>

<script>
import Skill from './Skill.vue';

export default {
  name: 'about-section',
  props: ['about'],
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

/*@media (min-wdith: 767px) {.u-sm-mh-0 {
  background-color: green;
  min-height: 0px !important;
}}*/
</style>
