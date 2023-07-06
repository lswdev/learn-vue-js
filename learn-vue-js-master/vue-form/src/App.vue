<template @submit="submitForm">
  <form>
    <div>
      <label for="">id : </label>
      <input id="username" type="text" v-model="username">
    </div>
    <div>
      <label for="password">pw : </label>
      <input id="password" type="password" v-model="password">
    </div>
    <button type="submit" @click="submitForm">login</button>
  </form>
</template>

<script>
export default {
  data: function() {
    return {
      username: '',
      password: '',
    }
  },
  methods: {
    submitForm: function(event) {
      console.dir(event)
      event.preventDefault();
      console.log(this.username, this.password)
    }
  }
}

/* 
  vue create vue-form
  cd vue-form
  npm run serve(npm start)
*/
</script>
<style lang="">
  
</style>