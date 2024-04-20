

<template>
  <!--Text interpolation -->
 <div>Hello {{ name }}  </div> <br>
 <div v-text="channel"></div><br>
 <h3 v-text="facebook"></h3><br>
 <p v-html="channel_html"></p><br>
 <p v-html="hack"></p><br>
 <h1 v-bind:id='headingId'>Heading</h1><br>
 <button v-bind:disabled="isDisabled">click me disabled</button><br>
 <button v-bind:disabled="isNotDisabled">click me not disabled</button><br>
 <h1 class="underline">underlined text </h1><br>
 <h1 v-bind:class="success">danger </h1><br>
 <h1 v-bind:class="isPromoted && 'promoted'">Pomoted movie </h1><br>
 <h1 v-bind:class="isSoldOut ? 'soldout' : 'new'">soldout? movie </h1><br>
 <h1 v-bind:class="[isPromoted && 'promoted', isSoldOut ? 'soldout' : 'new']">Array conditional movie  </h1><br>
 <h1 v-bind:class="{
  promoted:isPromoted,
  new:!isSoldOut,
  soldout:isSoldOut
 }">Object conditional movie  </h1><br>
 <h2 v-bind:style="{
  color:highlightColor,
  'font-size':headerSize +'px',
  fontSize:headerSize +'px',
 }">Inline Style</h2><br>
  <h2 v-bind:style="styleObject">style object</h2><br>
  <div v-bind:style="[baseStyleObject , successStyleObject]">success style array</div><br>
  <div v-bind:style="[baseStyleObject , dangerStyleObject]">danger style array</div><br>
 
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
      hack:`<a href='#' onclick='alert("You have been hacked.")'>Win a prize</a>`,
      headingId:"Heading",
      isDisabled:true,
      isNotDisabled:false,
      danger:"danger",
      success:"success",
      isPromoted:true,
      isSoldOut:true,
      highlightColor:"orange",
      headerSize:50,
      styleObject:{
      color:"orange",
      fontSize:50+'px',
      padding:20+'px',
      },
      baseStyleObject:{
        fontSize:'50px',
        padding:'20px',
      },
      successStyleObject:{
        color:'green',
        backgroundColor:'lightgreen',
        border:'1px solid green',

      },
        dangerStyleObject:{
        color:'darkred',
        backgroundColor:'red',
        border:'1px solid darkred',

      },
    };
  }
}
</script>