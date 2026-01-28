<template>
  <div class="container-box">
    <h2>{{ count }}</h2>
    <CounterButtons  @change-count="handleCountChange"/>
  </div>
</template>

<script>
  import CounterButtons from './components/CounterButtons.vue';
export default {
  name: 'App',
  components: {
    CounterButtons

  },
  data() {
    return {
      count: 0
    }
  },
  methods: {
    handleCountChange(action, value = 1) {
      switch (action) {
        case 'increment':
          this.count += value
          break
        case 'decrement':
          this.count -= value
          break
        case 'reset':
          this.count = 0
          break    
      }
    }
  }
}
</script>

<style>
.container-box {
  display: flex;
  flex-direction: row;
  border: 1px solid black;
  padding: 10px;
  gap: 10px;
  justify-content: center;
}

.box {
  width: 30px;
  height: 30px;
  background-color: red;
  align-items: center;
  display: flex;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  name-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
