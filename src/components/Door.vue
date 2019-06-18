<template>
  <div id="door">
    <div class="window">
      <div v-for="i in 6" :key="i.id"></div>
    </div>
    <div class="window">
      <div v-for="i in 6" :key="i.id"></div>
    </div>
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
  &>div {
    background-color: #7066ac;
    margin-left: 10px;
    margin: 15px;
    width: 55%;
    justify-self: center;
    &.window {
      background-color: #ffffffb5;
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      grid-template-rows: 1fr 1fr;
      div {
        border: 1px solid white;
      }
    }
  }
}
</style>
