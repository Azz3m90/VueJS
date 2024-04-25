<template>
 <div>
   <h3>This is a pop up</h3>
   <input type="text" v-model="name"/>
   <button @click="$emit('close',name)">Close Popup</button>
 </div>
</template>

<script>
export default {
 name:"Popup",
 data(){
  return {
   name:''
  }
 },
 setup () {
  return {}
 },
 emits:{
  close(name){
   if(!name){
    return false
   }else{
    return true
   }
  }
 }
}
</script>

<style lang="scss" scoped>

</style>