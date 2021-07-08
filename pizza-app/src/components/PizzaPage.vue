<template>
    <header class="App-header">
        <div class="pizza">
            <div class="pizza__slice">
              🍕
            </div>
            <h1 class="pizza__topping">
              {{topping}}
            </h1>
        </div>
        <form class="pizza__label">
          <label>Choose your topping:</label>
          <input v-on:change="consoleLog" />
          <label>Food coloring?:</label>
          <input />
        </form>
      </header>
</template>

<script>
export default {
  name: 'PizzaPage',
  props: {
    msg: String
  },
  data: () => ({
      topping: "cheese string",
      coloring: ""
  }),
  methods: {
      consoleLog: function (event) {

          console.log(event.target.value);
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.App-header {
  background-color: #282c34;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-size: calc(10px + 2vmin);
  color: white;
}

.App-link {
  color: #61dafb;
}

.pizza {
  position: relative;
  text-align: center;
  width: 50%;
  height: 22em;
}

.pizza__label {
  margin: 2em;
}

.pizza__slice {
  font-size: 20em;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.pizza__topping {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}



@keyframes App-logo-spin {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}
</style>
