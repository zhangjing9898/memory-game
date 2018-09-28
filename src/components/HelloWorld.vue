<template>
  <div class="game-panel">
    <dash-board></dash-board>
    <chess-board></chess-board>
    <footer></footer>
  </div>
</template>

<script>
import dashBoard from './dashboard/dashboard'
import chessBoard from './card/chessBoard'
import status from './footer/footer'

export default {

  components:{
    dashBoard,
    chessBoard,
    status
  }
}
</script>

<style scoped>
.game-panel {
  width: 450px;
  height: 670px;
  border: 4px solid #bdbdbd;
  border-radius: 2px;
  background-color: #faf8ef;
  padding: 10px;
  display: flex;
  flex-direction: column;
}

@media screen and (max-width: 450px) {
  .game-panel {
    width: 100%;
    height: 100%;
    justify-content: space-around;
  }
}
</style>
