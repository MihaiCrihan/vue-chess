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
    chestPositions: [
      {
        id: 'b1',
        positionX: 1,
        positionY: 0,
        isBlack: true,
        isQueen: false
      },
      {
        id: 'b2',
        positionX: 3,
        positionY: 0,
        isBlack: true,
        isQueen: false
      },
      {
        id: 'b3',
        positionX: 5,
        positionY: 0,
        isBlack: true,
        isQueen: false
      },
      {
        id: 'b4',
        positionX: 7,
        positionY: 0,
        isBlack: true,
        isQueen: false
      },
      {
        id: 'b5',
        positionX: 0,
        positionY: 1,
        isBlack: true,
        isQueen: false
      },
      {
        id: 'b6',
        positionX: 2,
        positionY: 1,
        isBlack: true,
        isQueen: false
      },
      {
        id: 'b7',
        positionX: 4,
        positionY: 1,
        isBlack: true,
        isQueen: false
      },
      {
        id: 'b8',
        positionX: 6,
        positionY: 1,
        isBlack: true,
        isQueen: false
      },
      {
        id: 'b9',
        positionX: 1,
        positionY: 2,
        isBlack: true,
        isQueen: false
      },
      {
        id: 'b10',
        positionX: 3,
        positionY: 2,
        isBlack: true,
        isQueen: false
      },
      {
        id: 'b11',
        positionX: 5,
        positionY: 2,
        isBlack: true,
        isQueen: false
      },
      {
        id: 'b12',
        positionX: 7,
        positionY: 2,
        isBlack: true,
        isQueen: false
      },
      {
        id: 'a1',
        positionX: 0,
        positionY: 5,
        isBlack: false,
        isQueen: false
      },
      {
        id: 'a2',
        positionX: 2,
        positionY: 5,
        isBlack: false,
        isQueen: false
      },
      {
        id: 'a3',
        positionX: 4,
        positionY: 5,
        isBlack: false,
        isQueen: false
      },
      {
        id: 'a4',
        positionX: 6,
        positionY: 5,
        isBlack: false,
        isQueen: false
      },
      {
        id: 'a5',
        positionX: 1,
        positionY: 6,
        isBlack: false,
        isQueen: false
      },
      {
        id: 'a6',
        positionX: 3,
        positionY: 6,
        isBlack: false,
        isQueen: false
      },
      {
        id: 'a7',
        positionX: 5,
        positionY: 6,
        isBlack: false,
        isQueen: false
      },
      {
        id: 'a8',
        positionX: 7,
        positionY: 6,
        isBlack: false,
        isQueen: false
      },
      {
        id: 'a9',
        positionX: 0,
        positionY: 7,
        isBlack: false,
        isQueen: false
      },
      {
        id: 'a10',
        positionX: 2,
        positionY: 7,
        isBlack: false,
        isQueen: false
      },
      {
        id: 'a11',
        positionX: 4,
        positionY: 7,
        isBlack: false,
        isQueen: false
      },
      {
        id: 'a12',
        positionX: 6,
        positionY: 7,
        isBlack: false,
        isQueen: false
      }
    ],
    newPositionX: 0,
    newPositionY: 0,
    count: 0,
    keepChessId: ''
  }),
  mounted() {
    //  for (let i = 1; i <= 8; i++) {
    //     for (let j = 1; j <= 4; j++) {
    //       this.chestPositions.push({
    //       id: `white${i}`,
    //       positionY: 1,
    //       isBlack: false,
    //       isQueen: false
    //   },)
    //   if(i % 2 === 0) {
    //     this.chestPositions.push({
    //       positionX: 1,
    //       isBlack: true,
    //       },)
    //   }
    //  }
    //  }


        // for(column, columnIndex) in row" :key="columnIndex">
        //   :class=" column === 1 ? 'white-cell' : 'black-cell'">
          
    // let posx = 1;
    // let val = 0;
    // let initx = 1;
    // for (let i = 1; i <= 7; i++) {
    //   if ((i % 2) === 0 ) {
    //     // val = 1;
    //     // this.chestPositions.push({
    //     //   positionX: 1,
    //     //
    //     // },)
    //   } else {
    //     console.log(i + "-------------")
    //   }
    // }
    // for (let white = 1; white <= 12; white++) {
    //   let posy = (white > 8 && white <= 12 ) ? 2 : (white <= 4)? 0 : (white > 4 && white <= 8 )? 1 : '';
    //   this.chestPositions.push({
    //     id: `white${white}`,
    //     positionX: 1,
    //     positionY: `${posy}`,
    //     isBlack: false,
    //     isQueen: false
    //   },)
    // }
    // for (let black = 1; black <= 12; black++) {
    //   let posy = (black > 8 && black <= 12 ) ? 7 : (black <= 4)? 5 : (black > 4 && black <= 8 )? 6 : '';
    //   this.chestPositions.push({
    //     id: `black${black}`,
    //     positionX: 6,
    //     positionY: `${posy}`,
    //     isBlack: true,
    //     isQueen: false
    //   },)
    // }
    // document.getElementById("json").textContent = document.body.innerHTML = JSON.stringify(this.chestPositions);
  },
  methods: {
    restartPage() {
      location.reload();
    },
    getIfGoTopLeft(chessIndex, rowIndex, columnIndex) {
      if (((this.chestPositions[chessIndex].positionX - 1) === rowIndex) && ((this.chestPositions[chessIndex].positionY - 1) === columnIndex)) {
        return true;
      }
    },
    getIfGoTopRight(chessIndex, rowIndex, columnIndex) {
      if (((this.chestPositions[chessIndex].positionX + 1) === rowIndex) && ((this.chestPositions[chessIndex].positionY - 1) === columnIndex)) {
        return true;
      }
    },
    getIfGoBottomLeft(chessIndex, rowIndex, columnIndex) {
      if (((this.chestPositions[chessIndex].positionX - 1) === rowIndex) && ((this.chestPositions[chessIndex].positionY + 1) === columnIndex)) {
        return true;
      }
    },
    getIfGoBottomRight(chessIndex, rowIndex, columnIndex) {
      if (((this.chestPositions[chessIndex].positionX + 1) === rowIndex) && ((this.chestPositions[chessIndex].positionY + 1) === columnIndex)) {
        return true;
      }
    },
    getChessCoordinate(positionX, positionY, id) {
      console.log(positionX, positionY, id, this.count)
     // if(this.count % 2 === 0 && this.count !== 0) {
     //   console.log("kill");
     // }
      this.count = this.count+1
      this.keepChessId = id;
      this.newPositionX = positionX;
      this.newPositionY = positionY;
    },
    getCoordinate(rowIndex, columnIndex) {
      console.log(rowIndex, columnIndex)
      const chessIndex = this.chestPositions.findIndex(item => item.id === this.keepChessId)
          // && (this.count % 2 === 0 && this.count !== 0)
      if (
        this.getIfGoTopRight(chessIndex, rowIndex, columnIndex) ||
        this.getIfGoTopLeft(chessIndex, rowIndex, columnIndex) ||
        this.getIfGoBottomRight(chessIndex, rowIndex, columnIndex) ||
        this.getIfGoBottomLeft(chessIndex, rowIndex, columnIndex))
        {
        // if()
        this.chestPositions[chessIndex].positionX = rowIndex
        this.chestPositions[chessIndex].positionY = columnIndex
      }

    }
    // killChess () {
    //   this.chestPositions[chessIndex].positionX = 7
    //   this.chestPositions[chessIndex].positionY = 9  
    // }
  },
  props: {
    msg: String
  }
}
</script>

<template>
  <div class="hello">
    <pre id="json"></pre>
    <h1>{{ msg }}</h1>
    <div class="desk">
      <div v-for="chess in chestPositions" :key="chess.id">
        <img @click="getChessCoordinate(chess.positionX, chess.positionY, chess.id)" class="chest" alt="chess"
             style="position: absolute;"
             :style="{ left: (chess.positionX * 80) + 'px', top: (chess.positionY * 80) + 'px' }"
             :src="chess.isBlack ? require('../assets/black.png') : require('../assets/white.png')">
      </div>
      <div v-for="(row, rowIndex) in matrix" :key="rowIndex">
        <div v-for="(column, columnIndex) in row" :key="columnIndex">
          <div @click="getCoordinate(rowIndex,columnIndex)" :class=" column === 1 ? 'white-cell' : 'black-cell'">
            {{ rowIndex }},{{ columnIndex }}
          </div>
        </div>
        <br>
      </div>
    </div>
    <button @click="restartPage" class="reload-button">Reload Page</button>
  </div>
</template>
<style>
body {
  background: gray;
}

#app {
}
</style>
<style scoped>
.desk {
  margin: 0 auto;
  min-width: 640px;
  max-width: 640px;
  min-height: 640px;
  max-height: 640px;
  display: flex;
  color: white;
  position: relative;
  font-weight: bold;
}

.reload-button {
  padding: 10px 32px;
  margin-top: 42px;
  border: 1px solid #000;
  border-radius: 8px;
  font-weight: bold
}

.chest {
  width: 80px;
  height: 80px;
}

.white-cell {
  width: 80px;
  height: 80px;
  color: black;
  background-color: #ffffff;
}

.black-cell {
  color: white;
  width: 80px;
  height: 80px;
  background-color: #000000
}

.hello {
  max-width: 100%;
}

</style>
