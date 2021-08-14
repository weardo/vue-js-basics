<template>
  <div>Hello {{ name }}</div>  
  <div v-text="github"></div>
  <div v-html="github"></div>
  <div v-html="hack"></div>
  <h2 :id="headingId">Heading</h2>
  <button :disabled="isDisabled">Bind</button>
  <h2 class="underline">Underlined Text</h2>
  <h2 :class="status">Status</h2>
  <h2 :class="isPromoted && 'promoted'">Promoted Movie</h2>
  <h2 :class="isSoldout ? 'sold-out' : 'new'">Soldout? movie</h2>
  <h2 :class="['new', 'promoted']">New and Promoted Class</h2>
  <h2 :class="[isSoldout ? 'sold-out' : 'new', isPromoted && 'promoted']">New and Promoted Class</h2>
  <h2 :class="{
    promoted: isPromoted,
    new: !isSoldout,
    'sold-out': isSoldout
  }">Object Conditional Movie</h2>
  
  <h2 :style="{
      color: highlightColor,
      fontSize: headerSize + 'px',
      padding: '20px'
    }">Inline Style</h2>
    <h2 :style="headerStyleObject">Header Sytle Object</h2>

    <div :style="[baseStyleObject, successStyleObject]">Success Style</div>
    <div :style="[baseStyleObject, dangerStyleObject]">Success Style</div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      name:  'Are you ready',
      greet: 'Ratatat',
      github: '<h1>Weardo</h1>',
      hack: `<a href="#" onclick="alert('You have been hacked')">Hack me</a>`,
      headingId: 'heading',
      isDisabled: true,
      status: 'success',
      isPromoted: false,
      isSoldout: false,
      highlightColor: 'red',
      headerSize: 100,
      headerStyleObject: {
        color: 'orange',
        fontSize: '50px',
        padding: '20px'
      },
      baseStyleObject: {
        fontSize: '50px',
        padding: '10px',
      },
      successStyleObject: {
        color: 'green',
        backgroundColor: 'lightgreen',
        border: '1px solid green',
        padding: '20px'
      },
      dangerStyleObject: {
        color: 'darkred',
        backgroundColor: 'red',
        border: '1px solid darkred',
      }
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

.underline {
  text-decoration: underline;
}

.danger {
  color: red;
}

.success {
  color: green;
}

.promoted {
  font-style: italic;
}

.new {
  color: black;
}

.sold-out {
  color: red;
}
</style>
