<template>
  <div class="chessboard">
    <card v-for="(card,index) of cards" :key="index"></card>
  </div>
</template>

<script>
import Card from './card';

export default {
  data(){
    return {
      lastCard:null
    }
  },
  components:{
    Card
  }
}
</script>

<style scoped>
.chessboard {
  margin-top: 20px;
  width: 100%;
  background-color: #fff;
  height: 530px;
  border-radius: 4px;
  padding: 10px 5px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  align-content: space-around;
}

.container:nth-child(4n) {
  margin-right: 0px;
}

@media screen and (max-width: 450px) {
  .chessboard {
    height: 480px;
    padding: 10px 0px;
  }
}
@media screen and (max-width: 370px) {
  .chessboard {
    height: 450px;
  }
}
</style>
