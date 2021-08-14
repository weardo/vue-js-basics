<template>
  <div>
    <h2 v-if="num === 0">The number is zero </h2>
    <h2 v-else-if="num < 0">The number is negative </h2>
    <h2 v-else-if="num > 0">The number is positve </h2>
    <h2 v-else>Not a number </h2>
    <template v-if="display">
      <h2>Abhishek</h2>
      <h2>My Coding</h2>
      <h2>Vue</h2>
    </template>

    <h2 v-show="showElement">Using v-show</h2>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      num: 'Hi',
      display: true,
      showElement: true,
    };
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
