<script setup lang="ts">
const { data, status, refresh } = await useFetch('/api');
</script>

<template>
  <div>
    <!-- refresh -->
    <button @click="() => refresh()">
      refresh
    </button>

    <!-- status, data -->
    <table border="1">
      <tr>
        <td>status</td>
        <td>{{ status }}</td>
      </tr>
      <tr>
        <td>data</td>
        <td><pre>{{ data }}</pre></td>
      </tr>
    </table>
  </div>
</template>