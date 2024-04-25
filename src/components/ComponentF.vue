<template>
 <div>
  <h2>Component F</h2>
     <h3>the user name from App root Component is - {{ username }}</h3>
 </div>
</template>

<script>
export default {
 setup () {
  

  return {}
 },
 inject:['username']
}
</script>

<style lang="scss" scoped>

</style>