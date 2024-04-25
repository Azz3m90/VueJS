

<template>
  <Card></Card>
  <Card >Card Content</Card>
  <Card >
    <img src="https://picsum.photos/200" alt="photos">
  </Card>
  <Card >
    <h2>Card Content</h2>
  </Card>
  <Card>
    <template v-slot:header>
      <h3>header</h3>
    </template>
    <template v-slot:default>
        <img src="https://picsum.photos/200" alt="photos">
    </template>
    <template v-slot:footer>
      <button>view details</button>
    </template>
  </Card>
</template>

<script>
import Card from './components/Card.vue';

export default {
  name:"App",
  components:{
    Card
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