<template>
<div>
  <h2 v-once>{{name}}</h2>
  <button @click="name = 'Batman'">Change Name</button>
  <h2 v-pre>{{name}}</h2>
</div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return { 
      name: 'Abhishek',
    };
  },
  methods: {
    submitForm() {
      console.log('Form Values', this.formValues)
    }
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}

label {
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}

input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}

input[type='flex'], textarea, select {
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.42857143;
  color: #555;
  background-color: #FFF;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 4px;
}
</style>
