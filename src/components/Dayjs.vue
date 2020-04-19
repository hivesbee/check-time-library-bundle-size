<template>
  <div>
    <p>dayjs: {{ date }}</p>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

import dayjs from "dayjs";
// import 'dayjs/locale/ja'

const formatDate = (day: any) => {
  // dayjs.locale('ja')
  return dayjs(day).format('YYYY-MM-DD hh:mm:ss');
}

@Component
export default class Dayjs extends Vue {
  get date() {
    return formatDate(new Date());
  }
}
</script>
