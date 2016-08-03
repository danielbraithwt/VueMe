<template>
<div>
  <div class="Card">
    <div class="u-flex u-flexRow u-flexWrap">
      <div class="col-xs-12 u-p-0">
        <img class="Card--Image" v-bind:src="image" />
      </div>
      <div class="col-xs-12 u-p-0">
        <slot name="top"></slot>
      </div>

      <div class="col-xs-9 u-flex">
        <slot name="actions"></slot>
      </div>

      <div v-if="!alwaysExpanded" class="col-xs-3 u-flex u-flexJustifyContentCenter u-sm-hide">
        <div v-on:click="toggleExpanded" v-bind:class="{ 'Card-expand--expanded':expanded }" class="Ripple Card-expand">
          <img src="../../static/chevron-down.svg" />
        </div>
      </div>

      <div v-bind:class="{ 'Card-bottom--show':(expanded || alwaysExpanded) }" class="Card-bottom col-xs-12">
        <slot name="bottom"></slot>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'card',
  props: ['image', 'alwaysExpanded'],
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
