<template>
  <div id="door">
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
#door {
  background-color: #4039c3;
  height: 100%;
  width: 80%;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr;
  // grid-gap: 10px 20px;
  div {
    background-color: white;
    margin-left: 10px;
    margin: 15px;
  }
}
</style>
