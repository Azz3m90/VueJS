

<template>
<h2>Volume Tracker(0-10)</h2>
<h2>Current Volume - {{ volume }}</h2>
<input type="text" v-model="movie">
<input type="text" v-model="movieInfo.title">
<input type="text" v-model="movieInfo.actor">
<button @click="volume += 2">Increase</button>
<button @click="volume -= 2">Decrease</button>
<div>
  <button @click="movieList = movieList.concat('new pushed movie')">Add Movie</button>
</div>
</template>

<script>
export default {
  name:"App",
  data(){
    return {
      volume : 0 ,
      movie:'Batman',
      movieInfo:{
        title:'',
        actor:''
      },
      movieList:['AzzamMovie', 'Allam Movie']
    }
  },
  methods:{

},
  computed:{
    
},
watch:{
  volume(newValue, oldValue){
    if(newValue > oldValue &&newValue === 16){
      alert('hearing high level volume for a long time may damage your hearing')
    }
  },
  movie:{
    handler(newValue){
    console.log(`API has been called to fetch the movie name : ${newValue}`)},
    immediate:true,
   },
   movieInfo:
   {
    handler(newValue){
     console.log(`API has been called to fetch the movie name : ${newValue.title} and actor: ${newValue.actor}`)
    },
    deep:true
  },
  movieList:
   {
    handler(newValue){
     console.log(`movieList Upldated : ${newValue} `)
    },
    //deep:true
  },
}
}
</script>


<style scoped>

</style>