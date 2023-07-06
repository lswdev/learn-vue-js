<template>
  <div>
    <app-header :propsdata="str" @renew="renewStr"></app-header>
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
  },
  methods: {
    // AppHeader 에서 this.$emit()으로 받은 @renew 이벤트에 fuction을 연결
    renewStr: function() {
      this.str = 'hi~~';
    }
  }
}
</script>

<style lang="">
  
</style>