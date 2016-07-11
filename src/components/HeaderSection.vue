<template>
  <div class="u-background">

  </div>

    <div class="Container row Fill--height">
      <div class="col-xs-12 middle-xs center-xs u-flex u-flexWrap u-flexRow">
        <div class="col-xs-12 center-xs middle-xs u-flex u-flexWrap">
          <img class="Profile-Icon" src="../assets/profile-photo.jpg" />
          <h1 class="Profile-Text Fill--width">Daniel Braithwaite</h1>
        </div>
      </div>
    </div>

    <div class="row Fill--height u-overlay">
      <div class="col-xs-12 bottom-xs center-xs u-flex u-flexWrap u-flexRow">
        <div class="col-xs-12 bottom-xs u-flex u-flexWrap">
          <social></social>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Social from './Social.vue';

export default {
  name: 'header-section',
  components: {
    Social
  }
}
</script>

<style>
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
  font-size: 10vw;
  color: white;
}

.Icon {
    border-radius: 50%;
    margin: 10px;

    width: 50px;
    height: 50px;
}

@media (min-width: 950px) {.Icon {
    width: 100px;
    height: 100px;
}}

@media (min-width: 1500px) {.Icon {
    width: 150px;
    height: 150px;
}}
</style>
