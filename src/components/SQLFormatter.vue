<script lang="ts">
import { format } from 'sql-formatter';
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return { sql: "" };
  },

  computed: {
    formattedSql(): string {
      return format(this.sql);
    }
  }
});
</script>

<template>
  <textarea v-model="sql" style="width: 80em; height: 10em;" />

  <highlightjs language="sql" :code="formattedSql" style="text-align: left" />
</template>