<template>
<div>
  <h2>{{name}}</h2>
  <div>
    <button v-on:mouseover="name = 'Batman'">Change Name</button>
  </div>
  <h2>{{count}}</h2>
  <div>
    <button v-on:click="increment(1)">Increment</button>
    <button v-on:click="decrement(23)">Increment</button>
  </div>
</div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      name: 'Abhishek',
      count: 0
    };
  },
  methods: {
    add(a, b, c) {
      return a + b + c
    },
    multiply(num) {
      return num * this.baseMultiplier
    },
    increment(num) {
      this.count += num
    },
    decrement(num) {
      this.count -= num
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
