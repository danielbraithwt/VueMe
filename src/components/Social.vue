<template>
<div>
  <div class="Social">
    <template v-for="item in social">
      <a v-bind:href="item.url" v-on:click="logSocialEvent(item.name, item.label)">
        <div class="Social-icon Icon">
          <img class="Social-icon-image" v-bind:src="item.icon" />
        </div>
      </a>
    </template>
  </div>
</div>
</template>

<script>
export default {
  name: 'social',
  props: ['social'],
  methods: {
    logSocialEvent: function(action, label) {
      console.log("Social Event: " + action + ", " + label);
      ga('send', {
        hitType: 'event',
        eventCategory: 'Social',
        eventAction: action,
        eventLabel: label,
      });
    }
  }
}
</script>
