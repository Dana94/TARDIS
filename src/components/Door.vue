<template>
  <div id="door">
    <div class="side">
      <div>
        <div class="pane"></div>
        <div class="window">
          <div v-for="i in 6" :key="i.id"></div>
        </div>
        <div v-for="i in 7" :key="i.id" :class="{'pane': i % 2 != 0}"></div>
      </div>
    </div>
    <div class="side">
      <div>
        <div class="pane"></div>
        <div class="window">
          <div v-for="i in 6" :key="i.id"></div>
        </div>
        <div v-for="i in 7" :key="i.id" :class="{'pane': i % 2 != 0}"></div>
      </div>
    </div>
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
  .side {
    border: 1px solid black;
    width: 60%;
    margin: 0 auto;
    height: 100%;
    & > div {
      display: grid;
      grid-template: 15px 1fr 15px 1fr 15px 1fr 15px 1fr 15px / 1fr;
      border: 1px solid black;
      height: 100%;
      .window {
        background-color: #ffffffb5;
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: 1fr 1fr;
        width: 100%;
        div {
          border: 1px solid white;
        }
      }
      .pane {
        height: 11px;
        // background-color: #4039c3;
        border-bottom: 1px solid;
        border-top: 1px solid;
      }
      & > div {
        // background-color: #7066ac;
        // margin: 15px;
        // width: 55%;
        width: 100%;
        justify-self: center;
      }
    }
  }
}
</style>
