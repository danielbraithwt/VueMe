<template>
<div class="col-xs-12 col-sm-6 col-md-4 u-flex">
  <div class="Card">
    <div class="col-xs-12 u-flex u-flexJustifyContentCenter">
      <img class="InfoCard--Icon" v-bind:src="icon" />
      <!-- <h1 class="Section-header u-title">Quallifications</h1> -->
    </div>
    <div class="col-xs-12">
      <slot name="main"></slot>
    </div>

    <div class="col-xs-12">
      <slot name="bottom"></slot>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'info-card',
  props: ['icon'],
}
</script>

<style>
.InfoCard--Icon {
  margin-top: 10px;
}
</style>
