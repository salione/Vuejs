<template>
<div>
  test child server
</div>
  <button @click="resetFn()">reset with callback</button>
</template>

<script>
export default {
  name: "ChildApp",
  props:{
    resetFn:Function
  },
  methods:{

  }
}
</script>

<style scoped>

</style>