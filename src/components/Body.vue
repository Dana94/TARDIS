<template>
  <div id="body">
    <door></door>
  </div>
</template>

<script>
import Door from "./Door.vue";
export default {
  components: {
    Door
  }
};
</script>

<style lang="scss" scoped>
$blue: #1e099c;
#body {
  height: 400px;
  background-color: $blue;
  width: 300px;
  margin: 0 auto;
}
</style>
