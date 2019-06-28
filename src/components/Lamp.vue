<template>
  <div class="lamp">
    <div class="top-part">
      <div class="top"></div>
      <div class="base"></div>
      <div class="bar-container">
        <div class="bar"></div>
        <div class="bar"></div>
      </div>
    </div>
    <div class="bulb"></div>
    <div class="base"></div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
$blue: #1e099c;
$light-off: #f5f5dc;
$light-on: #ffff70;

.lamp {
  position: relative;
  .top-part {
    margin-bottom: -1.875rem;
    .top {
      border-bottom: 3px solid $blue;
      border-left: 8px solid transparent;
      border-right: 8px solid transparent;
      height: 0px;
      margin: 0 auto;
      width: 15px;
    }
    .bar-container {
      display: flex;
      justify-content: center;
      .bar {
        background-color: $blue;
        height: 30px;
        width: 3px;
        margin: 0 12px;
      }
    }
  }
  .bulb {
    animation: pulse 5s infinite;
    height: 30px;
    width: 30px;
    margin: 0 auto;
    border-radius: 50%;
  }
  .base {
    background-color: $blue;
    height: 7px;
    width: 37px;
    margin: 0 auto;
  }
}

@keyframes pulse {
  0% {
    background-color: $light-off;
  }
  100% {
    background-color: $light-on;
  }
}
</style>
