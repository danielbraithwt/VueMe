<template>
<div class="Icon Skill Skill--{{color}}">
  <p class="Skill-text">{{name}}</p>
</div>
</template>

<script>
export default {
  name: 'skill',
  props: ['name',
          'color'
        ]
}
</script>

<style>
.Skill {
  display: flex;
  background-color: lightgrey;
  text-align: center;
  justify-content: center;
  align-items: center;
}

.Skill-text {
  font-weight: bold;
  color: white;
}

/* JS */
.Skill--yellow {
  background-color: #F1BF26;
}

/* Java */
.Skill--red {
  background-color: #ED1C24;
}

/* SASS */
.Skill--pink {
  background-color: #C6538C;
}

/* Ember */
.Skill--amber {
  background-color: #DD6A58;
}

/* Git */
.Skill--brown {
  background-color: brown;
}

/* Vue */
.Skill--green {
  background-color: #4FC08D;
}
</style>
