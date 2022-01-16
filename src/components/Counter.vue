<script setup lang="ts">
import { ref } from 'vue';

const count = ref(0)
</script>

<template>
  <button type="button" @click="count++">count is: {{ count }}</button>
  <button type="button" @click="count--">1減らす</button>
  <button type="button" @click="count *= 2">2倍にする</button>
  <button type="button" @click="count = 0">リセット</button>
  <br />
</template>