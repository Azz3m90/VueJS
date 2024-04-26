

<template>
   <NameList>
    <template v-slot:default="slotProps">
      {{ slotProps.firstName }}
    </template>
   </NameList>
   <NameList>
    <template v-slot:default="slotProps">
        {{ slotProps.lastName }},{{ slotProps.firstName }}
    </template>
   </NameList>
   <NameList>
    <template v-slot:default="slotProps">
      {{ slotProps.firstName }} , {{ slotProps.lastName }}
    </template>
   </NameList>
</template>

<script>
import NameList from './components/NameList.vue';

export default {
  name:"App",
  components:{
    NameList
  },
  data(){
    return {

    }
  },

  
  methods:{

},
  computed:{
    
},
watch:{

}
}
</script>


<style >
html, body {
  height: 100vh;
  display: block;
  justify-content: center;
  align-items: center;
  font-family: Arial, sans-serif;
}

#app {
  text-align: center;
  display: block;
}

h1, h2, h3, div, p {
  display: block;
  margin: 10px 0; /* Adjust margin as needed */
}
</style>