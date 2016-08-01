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

<style>
.Social {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding-bottom: 10px;
}

.Social-icon {
  display: flex;
  justify-content: center;
  align-items: center;

  box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
  background-color: white;
}

.Social-icon-image {
  width: 50%;
  height: 50%;
}
</style>
