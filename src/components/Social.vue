<template>
  <div class="Social">
    <div class="Social-icon Icon">
      <img class="Social-icon-image" src="../assets/mark-github.svg" />
    </div>

    <div class="Social-icon Icon">
      <img class="Social-icon-image" src="../assets/mail.svg" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'social'
}
</script>

<style>
.Social {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  padding: 20px;
}

.Social-icon {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: lightgrey;
}

.Social-icon-image {
  width: 50%;
  height: 50%;
}
</style>
