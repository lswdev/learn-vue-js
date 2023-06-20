<template>
  <div class="hello">
    <span v-bind="objectOfAttrs">되나</span>
    <h1>{{ msg }}</h1>
    <p>
      Vue Cli 테스트중<br>
      건들지
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">마세요</a>.
    </p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
}
const objectOfAttrs = {
  id: 'testId',
  class: 'testClass'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
