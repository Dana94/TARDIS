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
$blue: #1e099c;

#roof {
  .row {
    background-color: $blue;
    margin: 0 auto;
  }
  // https://css-tricks.com/the-shapes-of-css/ for Trapezoid help
  .triangle {
    border-bottom: 14px solid $blue;
    border-left: 108px solid transparent;
    border-right: 108px solid transparent;
    height: 0px;
    width: 34px;
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
