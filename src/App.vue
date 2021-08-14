<template>
  <h2>Add Method: {{add(1, 2, 3)}}</h2>
  <h2>Add Method: {{add(3, 5, 6)}}</h2>
  <h2>multiply Method: {{multiply(baseValue)}}</h2>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      baseMultiplier: 5,
      baseValue: 3
    };
  },
  methods: {
    add(a, b, c) {
      return a + b + c
    },
    multiply(num) {
      return num * this.baseMultiplier
    }
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
