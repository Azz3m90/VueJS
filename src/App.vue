

<template>
  <!--Text interpolation -->
 <div>Hello {{ name }}  </div> 
 <div v-text="channel"></div>
 <h3 v-text="facebook"></h3>
 <p v-html="channel_html"></p>
 <p v-html="hack"></p>
 
</template>

<style scoped>

</style>
<script>
export default {
  name:"App",
  data(){
    return {
      name:'Azzam',
      channel:'Eng.Azzam Aziz Ali',
      facebook:'Azzam Aziz Ali',
      channel_html:"<h3><i>channel</i></h3>",
      hack:`<a href='#' onclick='alert("You have been hacked.")'>Win a prize</a>`
    };
  }
}
</script>