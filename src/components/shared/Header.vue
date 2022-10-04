<template>
<div>
  <p>my header fields</p>
  user:{{ username }}
  <br/>
  switch user:{{ switchUser() }}
  <button @click="resetUser()">reset</button>
</div>
</template>

<script>
export default {
  //recive value from parent
  props:['username'],
  name: "header-app",
  methods:{
    switchUser(){
      return this.username.split("").reverse().join("");
    },
    //send value to parent

    resetUser(){
      this.resetusername = 'roxo';
      this.$emit('usernameWasReset',this.resetusername)
    },


  }
}
</script>

<style scoped>
p{ border: 1px solid red}
</style>