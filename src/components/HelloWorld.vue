<script>
export default {
  name: 'HelloWorld',
  data: () => ({
    matrix: [
      [1, 0, 1, 0, 1, 0, 1, 0],
      [0, 1, 0, 1, 0, 1, 0, 1],
      [1, 0, 1, 0, 1, 0, 1, 0],
      [0, 1, 0, 1, 0, 1, 0, 1],
      [1, 0, 1, 0, 1, 0, 1, 0],
      [0, 1, 0, 1, 0, 1, 0, 1],
      [1, 0, 1, 0, 1, 0, 1, 0],
      [0, 1, 0, 1, 0, 1, 0, 1]
    ],
    ch_black: [
      ["0.0", "2.0", "4.0", "6.0"],
      ["1.1", "3.1", "5.1", "7.1"],
      ["0.2", "2.2", "4.2", "6.2"],
    ],

// координаты черных шашек
  ch_white: [
      "0.5", "2.5", "4.5", "6.5",
      "1.6", "3.6", "5.6", "7.6",
      "0.7", "2.7", "4.7", "6.7",
    ]
  }),
  methods: {
    getCoordinate (rowIndex, columnIndex) {
      console.log(rowIndex, columnIndex)
    }
  },
  props: {
    msg: String
  }
}
</script>

<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="desk">
      <div :key="posBlackIndex" v-for="(pos, posBlackIndex) in ch_black">
        <img :key="posWhiteIndex" v-for="(col, posWhiteIndex) in pos"  class="chest" src="../assets/black.png" alt="black" style="position: absolute;"
             :style="{ left: (col * 160) + 'px', top: (pos * 2) + 'px' }  ">
      </div>
      <div v-for="(row, rowIndex) in matrix" :key="rowIndex">
        <div v-for="(column, columnIndex) in row" :key="columnIndex">
          <div @click="getCoordinate(rowIndex,columnIndex)" :class=" column === 1 ? 'white-cell' : 'black-cell'">
            {{ rowIndex }},{{columnIndex}}
          </div>
        </div>
        <br>
      </div>
      <img class="chest" src="../assets/white.png" alt="black" style="position: absolute; bottom: 0"
           :style="{ left: (2 * 80) + 'px' }">
    </div>
  </div>
</template>
<!--          {{ rowIndex }},{{columnIndex}},<b>{{column}}</b>-->
<!-- Add "scoped" attribute to limit CSS to this component only -->
<!--      <div v-for="(item, index) in 8" :key="index">-->
<!--        <div v-for="(column, index) in 8" :key="index" :class="((column + item) % 2 === 0) ? 'white-cell' : 'black-cell'">-->
<!--          {{ item }} ; {{ column }}-->
<!--        </div>-->
<!--      </div>-->
<style>
  body {
    background: gray;
  }
</style>
<style scoped>
  .desk {
    min-width: 640px;
    max-width: 640px;
    min-height: 640px;
    max-height: 640px;
    display: flex;
    color: white;
    position: relative;
    font-weight: bold;
  }
  .chest {
    width: 80px;
    height: 80px
  }

  .white-cell {
    height: 80px;
    width: 80px;
    color: black;
    background-color: #ffffff;
  }

  .black-cell {
    height: 80px;
    width: 80px;
    background-color: #000000
  }

</style>
