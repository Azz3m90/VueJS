

<template>
<!--<Greetings name="Azzam" heroName="Batman"/>
 <Greetings name="Allam" heroName="Superman"/>
<Greetings name="Abeer" heroName="Wonder Woman "/>
<Greetings :name="name" :heroName="channel"/> -->
<!-- <Article id="my-article" :likes="50" :isPublished="true" /> 
<h1>App Component username  - {{ name }}</h1>
<ComponentC />-->
<!-- <button @click="showPopup = true"> Show Popup</button>
<Popup v-show="showPopup" @close="closePopup"/> 
<input type="text" v-model="name" />-->
<Input  v-model="name"/>
</template>

<script>
//import Greetings from './components/Greetings.vue';
/* import Article from './components/Article.vue' */
/* import ComponentC from './components/ComponentC.vue'; */
/* import Popup from './components/Popup.vue'; */
import Input from './components/Input.vue';
export default {
  name:"App",
  components:{
    //Greetings,
    //Article,
    //ComponentC,
    /* Popup, */
    Input,
  },
  data(){
    return {
     // name:'Eng.Azzam Aziz Ali',
      //channel:'Azzam Aziz Ali',
      /* showPopup:false, */
      name:''
    }
  },
/*   provide(){
    return {
      username: this.name,
    } 
  },*/
  
  methods:{
/*     closePopup(name){
      this.showPopup = false
      console.log('name sent by a child component is : ',name)
    } */
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