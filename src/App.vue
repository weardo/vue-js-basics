<template>
<div>
  <template v-for="name in names" >
    <h2 v-if="name==='Diana'" :key="name">{{name}}: </h2>
    
  </template><br>
  <button @click="shuffle">Shuffle!</button>
</div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      names: ['Bruce', 'Clark', 'Diana', 'Barry'],
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
