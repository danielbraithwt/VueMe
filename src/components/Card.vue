<template>
<div class="col-xs-12 col-sm-6 col-md-4">
  <div class="Card">
    <div class="u-flex u-flexRow u-flexWrap">
      <div class="col-xs-12 u-p-0">
        <img class="Card--Image" v-bind:src="image" />
      </div>
      <div class="col-xs-12 u-p-0">
        <slot name="top"></slot>
      </div>

      <div  v-bind:class="{ 'Card-bottom--show':expanded }" class="Card-bottom col-xs-12 u-p-0">
        <slot name="bottom"></slot>
      </div>

      <div class="col-xs-12 center-xs u-flex u-p-0 u-sm-hidden">
        <div v-on:click="toggleExpanded" v-bind:class="{ 'Card-expand--expanded':expanded }" class="Card-expand">
          <img src="../../static/chevron-down.svg" />
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'card',
  props: ['image'],
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

<style>
.Card--Image {
  width: 100%;
}

.Card-expand {
  width: 50px;
  height: 50px;

  margin-bottom: -40px;

  box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);

  border-radius: 50%;

  background-color: white;

  display: flex;
  justify-content: center;
}

.Card-expand img {
  transform: rotate(0deg);
  transition: transform 600ms cubic-bezier(0.645, 0.045, 0.355, 1);
}

.Card-expand--expanded img {
  transform: rotate(180deg);
}

.Card-bottom {
  max-height: 0px;
  overflow: hidden;
  transition: max-height 400ms cubic-bezier(0.645, 0.045, 0.355, 1);

  padding-left: 20px;
  padding-right: 20px;
}

.Card-bottom--show {
  max-height: 1000px;
}

@media (min-width: 767px) {.Card-bottom {
    max-height: 1000px;
}}
</style>
