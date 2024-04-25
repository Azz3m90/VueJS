

<template>
<Greetings name="Azzam" heroName="Batman"/>
<Greetings name="Allam" heroName="Superman"/>
<Greetings name="Abeer" heroName="Wonder Woman "/>
<Greetings :name="name" :heroName="channel"/>
</template>

<script>
import Greetings from './components/Greetings.vue';
export default {
  name:"App",
  components:{
    Greetings,
  },
  data(){
    return {
      name:'Eng.Azzam',
      channel:'Azzam Aziz Ali'
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


<style scoped>

</style>