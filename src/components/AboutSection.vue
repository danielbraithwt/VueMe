<template>
<div>
  <div class="Container">
    <div class="row">
      <div class="col-xs-12 center-xs">
        <h1 class="Title">Me!</h1>
      </div>
    </div>
    <div class="MasonryColumn MasonryColumn--balanced">
      <card class="col-xs-12 MasonryColumn-Item" :always-expanded="true"
                                                 :image="about.aboutme.image">
        <h1 slot="top" class="Card-title">About Me</h1>
        <p slot="top" class="Card-subtitle">Subtitle</p>

        <p slot="bottom">{{ about.aboutme.text }}</p>
      </card>


      <card class="col-xs-12 MasonryColumn-Item" :always-expanded="true"
                                                 :image="about.experence.image">
        <h1 slot="top" class="Card-title">Experence</h1>
        <p slot="top" class="Card-subtitle">Subtitle</p>

        <p slot="bottom">{{ about.experence.text }}</p>
        <div slot="bottom" class="row">
          <skill v-for="skill in about.experence.skills"
                  :name="skill.name" :color="skill.color"></skill>
        </div>
      </card>

      <card class="col-xs-12 MasonryColumn-Item" :always-expanded="true"
                                                 :image="about.quallifications.image">
        <h1 slot="top" class="Card-title">Quallifications</h1>
        <p slot="top" class="Card-subtitle">Subtitle</p>

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
