<template>

  <h3 v-for="name in names":key="name.firstName">
   <slot :firstName="name.firstName" :lastName="name.lastName"></slot>
  </h3>

</template>

<script>
export default {
 name:"NameList",
 setup () {
  

  return {}
 },
 data(){
  return {
   names:[
    {
     firstName:'Azzam',
     lastName:"Ali"
    },{
     firstName:'Allam',
     lastName:"Ali"
    },{
     firstName:'Mohammad',
     lastName:"Ali"
    }    
   ]
  }
 }
}
</script>

<style lang="scss" scoped>

</style>