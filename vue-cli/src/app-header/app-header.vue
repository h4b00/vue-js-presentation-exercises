<template>
  <div id="header">
    <user-info>Hi I am from Slot</user-info>
  </div>
</template>
<script>
  import { UsersInfo } from './users-info.vue'
  export default {
    components:{
      'user-info': UsersInfo
    },
  }
</script>
<style>
  #header {
    width: 100%;
    height: 100px;
    border-bottom: 1px solid black;
  }
</style>
