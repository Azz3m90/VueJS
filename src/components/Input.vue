<template>
 <div>
  <input type="text" :value="modelValue" @input="$emit('update:model-value', $event.target.value)"/>
 </div>
</template>

<script>
export default {
 name:'Input',
 props:{
  modelValue:String
 },
 setup () {
  

  return {}
 }
}
</script>

<style  scoped>
input[type="text"],
input[type="password"],
input[type="email"],
input[type="number"],
input[type="tel"],
input[type="url"],
input[type="search"],
textarea {
  width: 100%;
  padding: 10px;
  margin-bottom: 15px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box; /* Ensures padding and border are included in the element's total width and height */
  font-family: Arial, sans-serif;
  font-size: 16px;
}
</style>