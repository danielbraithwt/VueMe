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
