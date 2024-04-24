

<template>
  <h1 v-once>{{ name }}</h1>
<button @click="name = 'Ali'">change name </button>
<h1 v-pre>{{ name }}</h1>
</template>

<style scoped>
  .underline{
    text-decoration: underline;
  }
  .danger{
    background-color: red;
  }
    .success{
    background-color: green;
  }
  .promoted{
    font-style: italic;
  }
  .new{
    color: olive;
  }
  .soldout{
    color: red;
  }
  h1,h2,h3,h3{
    display: block;
  }
</style>
<script>
export default {
  name:"App",
  data(){
    return {
      name:"Azzam",
    }
  },
}
</script>