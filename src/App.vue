<template>
  <div id="app">
    <dayjs />
    <date-fns />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

import Dayjs from "./components/Dayjs.vue";
import DateFns from "./components/DateFns.vue";

@Component({
  components: {
    Dayjs,
    DateFns
  }
})
export default class App extends Vue {}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
