<template>
  <div class="lamp">
    <div class="top"></div>
    <div class="base"></div>
    <!-- <div>
      <div class="bar"></div>
      <div class="bar"></div>
    </div> -->
    <div class="bulb"></div>
    <div class="base"></div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.lamp {
  position: relative;
  margin: 0 auto;
  .top {
    border-bottom: 3px solid #1e099c;
    border-left: 8px solid transparent;
    border-right: 8px solid transparent;
    height: 0px;
    margin: 0 auto;
    width: 15px;
  }
  // .bar {
  //   background-color: #1e099c;
  //   height: 30px;
  //   width: 30px;
  //   margin: 0 auto;
  // }
  .bulb {
    background-color: #cbc8de;
    height: 30px;
    width: 30px;
    margin: 0 auto;
    border-radius: 50%;
  }
  .base {
    background-color: #1e099c;
    height: 7px;
    width: 37px;
    margin: 0 auto;
  }
}
</style>
