<script setup lang="ts">
import { computed, ref } from 'vue';
import { format } from 'sql-formatter';

const sql = ref('');

const formattedSql = computed(() => format(sql.value));
</script>

<template>
  <textarea v-model="sql" style="width: 80em; height: 10em;" />

  <highlightjs language="sql" :code="formattedSql" style="text-align: left" />
</template>