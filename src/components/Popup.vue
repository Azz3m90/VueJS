<template>
 <div>
   <h3>This is a pop up</h3>
   <button @click="$emit('close','Azzam')">Close Popup</button>
 </div>
</template>

<script>
export default {
 name:"Popup",
 setup () {
  return {}
 },
 emits:['close']
}
</script>

<style lang="scss" scoped>

</style>