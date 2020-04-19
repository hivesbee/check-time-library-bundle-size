<template>
  <div>
    <p>date-fns: {{ currentDate }}</p>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

// import { format } from "date-fns/fp"; // これだとエラー ( TreeShaking するならこっち )
import { format } from "date-fns"; // これだと動く

const formatDate = (day: any) => {
  return format(day, 'yyyy-MM-dd hh:mm:ss');
}

@Component
export default class DateFns extends Vue {
  get currentDate() {
    return formatDate(new Date());
  }
}
</script>
