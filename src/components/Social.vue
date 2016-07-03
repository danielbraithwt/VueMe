<template>
  <div class="Social">
    <div class="Social-icon">

    </div>

    <div class="Social-icon">

    </div>

    <div class="Social-icon">

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
  justify-content: center;
  flex-wrap: wrap;
}

.Social-icon {
  width: 50px;
  height: 50px;

  border-radius: 50%;

  background-color: lightgrey;

  margin: 10px;
}
</style>
