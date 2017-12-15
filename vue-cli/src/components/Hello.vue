<template>
  <div>
    <h1>{{ welcomeMsg }} {{ intialMsg }}</h1>
    <button @click="emitPlease()">Please Update</button>
  </div>
</template>
<script>
  import { eventBus } from '../main.js'
  export default {
   props: {
     'welcome-msg': {
       default: 'Hello from default'
     },
   },
    data() {
     return {
       intialMsg: 'Hi',
       class: 'active'
     }
    },
    methods: {
     emitPlease(){
       // this.$emit('pleaseUpdate',this.intialMsg)
       eventBus.$emit('pleaseUpdate', this.intialMsg)
     }
    }
  }
</script>
<style>
</style>
