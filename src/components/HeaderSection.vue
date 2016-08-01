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

<style>
/*.NavBar {
  padding: 2em;
  justify-content: flex-end;
}

.NavBar-Item {
  padding-left: 2em;
  font-weight: bold;

  text-decoration: none;
}

.NavBar-Item:hover {
  text-decoration: underline;
}*/

.u-flex {
  display: flex;
}

.u-flexWrap {
  flex-wrap: wrap;
}

.u-flexRow {
  flex-direction: row;
}

.u-flexJustifyContentCenter {
  justify-content: center;
}

.u-overlay {
  position: absolute;
  top: 0;
  left: 0;
}

.Profile-Icon {
  border-radius: 50%;

  width: 60%;

  border-style: solid;
  border-color: white;
  border-width: thick;
}

.Profile-Text {
  /*font-size: 10vw;*/
  color: white;
}

.Icon {
    border-radius: 50%;
    margin: 10px;

    width: 50px;
    height: 50px;
}

/*@media (min-width: 950px) {.Icon {
    width: 100px;
    height: 100px;
}}

@media (min-width: 1500px) {.Icon {
    width: 150px;
    height: 150px;
}}*/
</style>
