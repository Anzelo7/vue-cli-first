<template>
  <div id="app">
    <img alt="Vue logo" :src="imgUrl" />
    Ciao!
    <p class="red">{{ saluto }}</p>
    <div v-for="(item, index) in test" :key="index">
      {{ item }}
      <FirstComponent />
    </div>
  </div>
</template>

<script>

import FirstComponent from './components/first-component.vue'


export default {
  name: 'App',
  data() {
    return {
      saluto: 'hello world',
      test: [1, 4, 8, 12, 1, 6],
      imgUrl: './assets/logo.png'
    };
  },
  components:{
    FirstComponent
  }
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>