<template>
  <div id="app">
    <header-app :username="name" @usernameWasReset="name = $event"></header-app>
    {{ status }}
    <button @click="changeUsername()">change</button>
    <server-status></server-status>
    <FooterApp :logo="logo"></FooterApp>
  </div>
<child-app :resetFn="callbackUser"></child-app>
</template>

<script>
import ServerStatus from "@/components/ServerStatus";
import FooterApp from "@/components/shared/Footer";
import HeaderApp from "@/components/shared/Header";
import ChildApp from "@/components/ChildApp";
export default {
  name: 'App',
  data:function (){
    return {
      status:'very good',
      name:'arman',
      logo:'my logo'
    }
  },
  components: {
    ChildApp,
    HeaderApp,
    FooterApp,
    ServerStatus,
    //send from parent to child

  },
  methods:{
    changeUsername(){
      this.name = 'change username'
    },
    callbackUser(){
      this.name = 'ishopsaz'
    }

  }
}
</script>

<style>

</style>


