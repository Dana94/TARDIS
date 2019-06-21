<template>
  <div id="footer">
    <div class="triangle"></div>
    <div class="row"></div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
#footer {
  .triangle {
    border-bottom: 10px solid #1e099c;
    border-left: 8px solid transparent;
    border-right: 8px solid transparent;
    height: 0px;
    width: 300px;
    margin: 0 auto;
  }
  .row {
    height: 20px;
    background-color: #1e099c;
    width: 316px;
    margin: 0 auto;
  }
}
</style>
