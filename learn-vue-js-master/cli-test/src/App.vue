<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <!-- 
      1. <hello-world></hello-world>
      2. <HelloWorld></HelloWorld>
      3. <HelloWorld/>
      모두 같은 컴포넌트를 호출한다.
      하지만 visual studio에서 컴포넌트 따라가기 기능을 사용하기 위해서는 1번 양식을 따라야 한다.(vue 공식 홈페이지 명시)
    -->
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
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
