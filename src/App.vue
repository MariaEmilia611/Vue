<template>
  <div class="container-box">
    <h3>{{ count }}</h3>
    <MyButton @increment="incrementCount"/>
  </div>
</template>

<script>
  import MyButton from './components/MyButton.vue';
export default {
  name: 'App',
  components: {
    MyButton

  },
  data() {
    return {
      count: 0
    }
  },
  methods: {
    incrementCount() {
      this.count++
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
