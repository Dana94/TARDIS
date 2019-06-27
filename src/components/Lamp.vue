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
    <!-- <div>
      <div class="bar"></div>
      <div class="bulb"></div>
      <div class="bar"></div>
    </div>-->
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
  .top-part {
    margin-bottom: -1.875rem;
    .top {
      border-bottom: 3px solid #1e099c;
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
        background-color: #1e099c;
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
    background-color: #1e099c;
    height: 7px;
    width: 37px;
    margin: 0 auto;
  }
}

@keyframes pulse {
  0% {
    background-color: #f5f5dc;
  }
  100% {
    background-color: #ffff70;
  }
}
</style>
