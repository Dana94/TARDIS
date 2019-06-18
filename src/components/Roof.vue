<template>
  <div id="roof">
    <div class="triangle"></div>
    <div class="row"></div>
    <div class="row"></div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
#roof {
  .row {
    background-color: #1e099c;
    margin: 0 auto;
    // border: 1px solid;
  }
  // https://css-tricks.com/the-shapes-of-css/ for Trapezoid help
  .triangle {
    border-bottom: 24px solid #1e099c;
    border-left: 108px solid transparent;
    border-right: 108px solid transparent;
    height: 0px;
    width: 39px;
    margin: 0 auto;
  }
  .row:nth-child(2) {
    width: 250px;
    height: 30px;
  }
  .row:nth-child(3) {
    height: 20px;
    width: 276px;
  }
}
</style>
