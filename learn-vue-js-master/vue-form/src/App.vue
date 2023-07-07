<template>
  <form @submit.prevent="submitForm"><!-- event.preventDefault 동일 -->
    <div>
      <label for="">id : </label>
      <input id="username" type="text" v-model="username">
    </div>
    <div>
      <label for="password">pw : </label>
      <input id="password" type="password" v-model="password">
    </div>
    <button type="submit">login</button>
  </form>
</template>

<script>
import axios from 'axios';

export default {
  data: function() {
    return {
      username: '',
      password: '',
    }
  },
  methods: {
    submitForm: function() {
      // event.preventDefault();   <---  vue에서는 v-on:submit.prevent를 사용
      console.log(this.username, this.password);

      var url = 'https://jsonplaceholder.typicode.com/users';
      var data ={
        username: this.username,
        password: this.password
      }
      axios.post(url, data)
      .then(function(response){
        console.log(response);
      })
      .catch( function(error){
        console.log(error);
      });      
      // http 프로토콜 을 이용한  http통신 라이브러리
      // 브라우저에서 서버로 데이터를 주고받기 위함

    }
  }
}

/* 
  vue create vue-form
  cd vue-form
  npm run serve(npm start)
*/

/* 
  npm i axios 
  에러 뜬다면 
  npm uninstall axios 후 npm i axios 실행.
*/
</script>
<style lang="">
  
</style>