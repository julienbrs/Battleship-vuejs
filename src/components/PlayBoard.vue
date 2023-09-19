<template>
  <div>
    <h2>{{ title }}</h2>
    <p>Rows: {{ rowsCount }}</p>
    <p>Columns: {{ columnsCount }}</p>
  </div>
</template>

<script>
export default {
  name: "PlayBoard",
  props: {
    title: {
      type: String,
      required: true,
    },
    rowsCount: {
      type: Number,
      required: true,
    },
    columnsCount: {
      type: Number,
      required: true,
    },
  },
};
</script>

<!-- You can add styles here if needed -->
