<template>
  <div>hello {{ status }}</div>
</template>

<script>
export default {
  name: "ServerStatus",
  data:function (){
    return {
      status:'Not good'
    }
  },
}
</script>

<style scoped>

</style>