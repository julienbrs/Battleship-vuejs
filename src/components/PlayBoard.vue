<template>
  <div class="playboard">
    <div class="title">{{ title }}</div>

    <div class="grid-container">
      <div v-for="row in rowsCount" :key="'row-' + row" class="line">
        <div
          v-for="column in columnsCount"
          :key="'cell-' + row + '-' + column"
          class="cell"
        ></div>
      </div>
    </div>
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

<style lang="scss" scoped>
.playboard {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.grid-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  border: 1px solid black;
  padding: 10px;
}
.line {
  margin: 0px;
  width: fit-content;
  display: flex;
  border-top: 1px solid black;
  border-bottom: 1px solid black;
  & + & {
    border-top: none;
  }
}
.cell {
  border-left: 1px solid black;
  border-right: 1px solid black;
  & + & {
    border-left: none;
  }
  height: 3vw;
  width: 3vw;
}
</style>