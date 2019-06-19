<template>
  <div id="door">
    <div class="side">
      <div>
        <div class="pane"></div>
        <div class="window">
          <div v-for="i in 6" :key="i.id"></div>
        </div>
        <div class="pane"></div>
        <div class="sign">
          <div>
            <div v-for="i in 3" :key="i.id" :class="{'pane': i % 2 != 0}"></div>
          </div>
        </div>
        <div v-for="i in 5" :key="i.id" :class="{'pane': i % 2 != 0}"></div>
      </div>
    </div>
    <div class="side">
      <div>
        <div class="pane"></div>
        <div class="window">
          <div v-for="i in 6" :key="i.id"></div>
        </div>
        <div class="pane"></div>
        <div class="shield"></div>
        <div v-for="i in 5" :key="i.id" :class="{'pane': i % 2 != 0}"></div>
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
    width: 100%;
    margin: 0 auto;
    height: 100%;
    & > div {
      display: grid;
      grid-template: 15px 1fr 15px 1fr 15px 1fr 15px 1fr 15px / 1fr;
      border: 1px solid black;
      height: 100%;
      width: 60%;
      margin: 0 auto;
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
      &>.pane {
        height: 11px;
        // background-color: #4039c3;
        border-bottom: 1px solid;
        border-top: 1px solid;
      }
      & > div {
        width: 100%;
        justify-self: center;
        &.sign {
          & > div {
            width: 80%;
            margin: 0 auto;
            border: 1px solid;
            height: 100%;
            display: grid;
            grid-template-rows: 10px 1fr 10px;
            grid-template-columns: 1fr;
          }
        }
      }
    }
  }
}
</style>
