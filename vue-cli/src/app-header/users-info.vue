<template>
  <div>
    <slot></slot>
    <span>{{ username }}</span>
    <span v-if="isLogged">
      <button @click="logoutUser()">Logout</button>
    </span>
    <span v-else>
      <button @click="loginUser()">Login</button>
    </span>
  </div>
</template>
<script>
  export default{
    data(){
      return {
        username: 'Unknow',
        isLogged: false
      }
    },
    methods: {
      logoutUser(){
        this.isLogged = false;
      },
      loginUser(){
        this.isLogged = true;
      }
    }
  }
</script>
<style scoped>
  div {
    float: right;
    font-size: 12px;
    font-weight: 700;
  }
</style>
