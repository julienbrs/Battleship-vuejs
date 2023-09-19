<template>
  <div class="battle-board">
    <div class="title">BattleShip</div>
    <PlayBoard title="Player" :columnsCount="10" :rowsCount="10" />
  </div>
</template>

<script>
import PlayBoard from "./PlayBoard.vue";

export default {
  name: "BattleBoard",
  components: {
    PlayBoard,
  },
};
</script>

<style lang="scss" scoped>
.title {
  font-size: 30px;
  font-weight: bold;
  margin-bottom: 30px;
}

.battle-board {
  padding: 30px;
}
</style>
