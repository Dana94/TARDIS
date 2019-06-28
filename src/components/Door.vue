<template>
  <div id="door">
    <div class="title"></div>
    <div class="door-panels">
      <div class="side">
        <div class="middle">
          <div class="pane"></div>
          <div class="window">
            <div v-for="i in 6" :key="i.id" :class="{'stained': i == 4 || i == 6}"></div>
          </div>
          <div class="pane"></div>
          <div class="sign">
            <div class="knob"></div>
            <div class="container">
              <div v-for="i in 3" :key="i.id" :class="{'pane': i % 2 != 0, 'poster': i % 2 == 0}"></div>
            </div>
          </div>
          <div v-for="i in 5" :key="i.id" :class="{'pane': i % 2 != 0}"></div>
        </div>
      </div>
      <div class="side">
        <div class="knob"></div>
        <div class="keyknob"></div>
        <div class="middle">
          <div class="pane"></div>
          <div class="window">
            <div v-for="i in 6" :key="i.id" :class="{'stained': i == 4 || i == 6}"></div>
          </div>
          <div class="pane"></div>
          <div class="shield">
            <img src="../assets/St._Johns_Ambulance.png" alt>
          </div>
          <div v-for="i in 5" :key="i.id" :class="{'pane': i % 2 != 0}"></div>
        </div>
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
  position: relative;
  .title {
    position: absolute;
    background-image: url("../assets/police_box_title.png");
    background-size: 100% 100%;
    background-repeat: no-repeat;
    height: 30px;
    width: 100%;
    top: -2.5rem;
    border: 3px solid #4039c3;
    left: -3px;
  }
  .door-panels {
    background-color: #4039c3;
    height: 100%;
    width: 80%;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr;
    margin-top: 0rem;
    .side {
      border: 1px solid black;
      border-bottom: none;
      width: 100%;
      margin: 0 auto;
      position: relative;
      & > div.middle {
        display: grid;
        grid-template: 15px 1fr 15px 1fr 15px 1fr 15px 1fr 15px / 1fr;
        border: 1px solid black;
        border-bottom: none;
        height: 100%;
        width: 68%;
        margin: 0 auto;
        .window {
          background-color: #ffffffb5;
          display: grid;
          grid-template-columns: 1fr 1fr 1fr;
          grid-template-rows: 1fr 1fr;
          width: 100%;
          div {
            border: 1px solid white;
            &.stained {
              background-color: #ffffff59;
            }
          }
        }
        .shield {
          display: flex;
          justify-content: center;
          align-items: center;
          img {
            height: 30px;
            width: auto;
          }
        }
        & > .pane {
          // height: 11px;
          border-bottom: 1px solid;
          border-top: 1px solid;
          &:last-child {
            border-bottom: none;
          }
          &:first-child {
            border-top: none;
          }
        }
        & > div {
          width: 100%;
          justify-self: center;
          &.sign {
            position: relative;
            .knob {
              position: absolute;
              background-color: #b9b9b9;
              border: 1px solid black;
              width: 4px;
              height: 15px;
              right: 2px;
              top: 2rem;
            }
            .container {
              width: 65%;
              margin: 0 auto;
              border: 1px solid;
              border-bottom: none;
              border-top: none;
              height: 100%;
              display: grid;
              grid-template-rows: 10px 1fr 10px;
              grid-template-columns: 1fr;
              .poster {
                background-image: url("../assets/sign.jpg");
                background-size: contain;
                background-repeat: no-repeat;
              }
            }
          }
        }
      }
      & > .knob {
        position: absolute;
        background-color: #b9b9b9;
        border: 1px solid black;
        width: 4px;
        height: 15px;
        right: 3px;
        left: 0.25rem;
        top: 9rem;
      }
      .keyknob {
        position: absolute;
        width: 8px;
        height: 8px;
        background-color: #b9b9b9;
        border-radius: 50%;
        left: 2px;
        bottom: 12rem;
        display: inline-block;
        border: 1px solid black;
      }
    }
  }
}
</style>
