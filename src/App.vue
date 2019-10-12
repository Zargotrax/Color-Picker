<template>
  <div id="app">
    <table >
      <tr>
        <td>
          <input
          type="number"
            v-model="num1"
            v-on:change="updateColor"
          ></input>
        </td>
        <td>
          Rouge          
        </td>
      </tr>
      <tr>
        <td>
          <input
          type="number"
          v-model="num2"
          v-on:change="updateColor"
          ></input>
        </td>
        <td>
          Vert
        </td>
      </tr>
      <tr>
        <td>
          <input
          type="number"
          v-model="num3"
          v-on:change="updateColor"
          ></input>
        </td>
        <td>
          Bleue
        </td>
      </tr>
    </table>
    <div id="color">
		</div>
	</div>
    </div>
    
  </div>
</template>

<script>
export default {
  name: 'app',
  data: function () {
    return {
      num1: 0,
      num2: 0,
      num3: 0,
    }; 
  },
  methods: {
    updateColor(){
      const colorSquare = document.getElementById("color")
      colorSquare.style.background = "rgb(" + this.num1 + ", " + this.num2 + ", " + this.num3 + ")";
    },
  },  
};
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

table{
  height: 10em;
  margin-left: auto;
  margin-right: auto;

}

#color{
  height: 8em;
  width : 8em;
  margin-left: auto;
  margin-right: auto;
  background-color: black;
}
</style>
