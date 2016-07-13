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
