<template>
 <h2>Articla component</h2>
 <h2 >{{ title }}</h2>
 <h2>Number of likes: {{ likes }}</h2>
 <h2>is published: {{ isPublished ? "Yes" : "No" }}</h2>
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
 }
}
</script>
<style >
</style>