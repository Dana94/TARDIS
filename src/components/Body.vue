<template>
  <div id="body">
    <door></door>
  </div>
</template>

<script>
import Door from './Door.vue';
export default {
  components: {
    Door
  }
}
</script>

<style lang="scss" scoped>
  #body {
    height: 400px;
    background-color: #1e099c;
    width: 300px;
    margin: 0 auto;
  }
</style>
