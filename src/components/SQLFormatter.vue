<script setup lang="ts">
import { format } from 'sql-formatter';
import { computed, ref } from 'vue';

const sql = ref("");
const formattedSql = computed(() => {
  return format(sql.value);
});
</script>

<template>
  <div class="container">
    <textarea v-model="sql" class="sqlInput" />
    <highlightjs language="sql" :code="formattedSql" class="sqlOutput" />
  </div>
</template>

<style>

.container {
  width: 50em;
  margin-left: 1em;
}
.sqlInput {
  width: 100%;
  height: 15em;
}

.sqlOutput {
  text-align: left;
}
</style>