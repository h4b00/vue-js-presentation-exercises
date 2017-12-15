<template>
  <hello :welcome-msg="test"></hello>
</template>
<script>
  import Hello from './components/hello'
  import { eventBus } from './main.js'

  export default {
    data() {
      return {
        test: 123
      }
    },
    methods: {
      updateWelcomeMsg(value){
        console.log(value)
        this.test = value;
      }
    },
    components:{
      hello: Hello
    },
    created() {
      eventBus.$on('pleaseUpdate', v => this.updateWelcomeMsg(v))
    }
  }
</script>
<style>
</style>
