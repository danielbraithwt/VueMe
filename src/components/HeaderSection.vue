<template>
    <div class="Fill--height Fill--width u-background">
      <div class="Container">
          <div class="Fill--height middle-xs center-xs row">
            <div class="col-xs-12 col-sm-8 col-md-6 col-lg-4">
              <img class="Profile-Icon" v-bind:src="photo" />
              <h1 class="Profile-Text mFill--width">{{ name }}</h1>
              <social class="u-sm-hide" :social="social"></social>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="u-overlay Fill--width Fill--height row bottom-xs">
      <div class="col-xs-12 center-xs ">
        <img src="../../static/ic_expand_more_white_48px.svg" />
      </div>
    </div>

    <div class="row Fill--height u-overlay">
      <div class="col-xs-12 bottom-xs center-xs u-flex u-flexWrap u-flexRow">
        <div class="col-xs-12 bottom-xs u-flex u-flexWrap">
          <social class="u-xs-hide u-sm-show":social="social"></social>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Social from './Social.vue';

export default {
  name: 'header-section',
  props: ['name', 'photo', 'social'],
  components: {
    Social
  }
}
</script>
