<template>
 <div>

   <h2>Articla component</h2>
   <h2 v-bind="$attrs">{{ title }}</h2>
   <h2>Number of likes: {{ likes }}</h2>
   <h2>is published: {{ isPublished ? "Yes" : "No" }}</h2>
 </div>

</template>
<script>
export default {
 name:'Article',
 props:{
  title:{
   type:String,
   required:true,
   default:"Article Default title"
  },
  likes:Number,
  isPublished:Boolean
 },

 inheritAttrs:false,
}
</script>
<style >
</style>