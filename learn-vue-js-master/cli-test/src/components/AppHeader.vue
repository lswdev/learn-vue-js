<template lang="">
  <div>
    <h1>{{ propsdata }}</h1>

    <button @click="sendEvent">send</button>
  </div>
</template>

<script>
export default { 
  props: ['propsdata'],
  methods: {
    sendEvent: function(){
      this.$emit('renew');
    }
  }
}
</script>

<style lang="">
  
</style>