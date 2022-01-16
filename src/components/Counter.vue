<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  props: {
    initial: { type: Number, default: 0 }
  },
  data() {
    return {
      count: this.initial
    }
  }
});
</script>

<template>
  <button type="button" @click="count++">count is: {{ count }}</button>
  <button type="button" @click="count--">1減らす</button>
  <button type="button" @click="count *= 2">2倍にする</button>
  <button type="button" @click="count = 0">リセット</button>
  <br />
</template>