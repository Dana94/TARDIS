<template>
  <div id="app">
    <transition-group name="fade">
      <template v-if="show">
        <app-lamp key="lamp"></app-lamp>
        <app-roof key="roof"></app-roof>
        <app-body key="app-body"></app-body>
        <app-footer key="app-footer"></app-footer>
      </template>
    </transition-group>
  </div>
</template>

<script>
import Roof from "./components/Roof.vue";
import Body from "./components/Body.vue";
import Footer from "./components/Footer.vue";
import Lamp from "./components/Lamp.vue";

export default {
  name: "app",
  data() {
    return {
      show: true
    };
  },
  components: {
    appBody: Body,
    appFooter: Footer,
    appRoof: Roof,
    appLamp: Lamp
  },
  created() {
    let vm = this;
    // transition fade in/out effect
    setInterval(() => {
      vm.show = !vm.show;
    }, 9000);
  }
};
</script>

<style lang="scss">
@import url("./assets/base.scss");

#app {
  margin-top: 60px;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 6s;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}
</style>
