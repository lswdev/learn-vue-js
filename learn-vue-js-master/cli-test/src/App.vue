<template>
  <div>
    <app-header :propsdata="str"></app-header>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

export default {
  data: function() {
    return {
      str: 'Header'
    }
  },
  components: {
    'app-header': AppHeader
  }
}
</script>

<style lang="">
  
</style>