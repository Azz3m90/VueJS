

<template>
<!--<Greetings name="Azzam" heroName="Batman"/>
 <Greetings name="Allam" heroName="Superman"/>
<Greetings name="Abeer" heroName="Wonder Woman "/>
<Greetings :name="name" :heroName="channel"/> -->
<!-- <Article id="my-article" :likes="50" :isPublished="true" /> -->
<h1>App Component username  - {{ name }}</h1>
<ComponentC />
</template>

<script>
//import Greetings from './components/Greetings.vue';
/* import Article from './components/Article.vue' */
import ComponentC from './components/ComponentC.vue';
export default {
  name:"App",
  components:{
    //Greetings,
    //Article,
    ComponentC,
  },
  data(){
    return {
      name:'Eng.Azzam Aziz Ali',
      channel:'Azzam Aziz Ali'
    }
  },
  provide(){
    return {
      username: this.name,
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