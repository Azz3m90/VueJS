

<template>
  <!--Text interpolation -->
 <!--<div>Hello {{ name }}  </div> <br>
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
  <p>v-bind shorthand:</p>
  <div :style="[baseStyleObject , dangerStyleObject]">danger style array</div><br>
 <h1 v-if="num === 0 ">the number is Zero</h1>
 <h1 v-else-if="num < 0"> the number is negative</h1>
 <h1 v-else-if="num > 0"> the number is positive</h1>
 <h1 v-else>the num is not a number</h1>
<template v-if="display">
 <h1>Azzam</h1>
 <h1>Aziz</h1>
 <h1>Ali</h1>
 </template>
 <h2 v-show="showElement">v-show Element</h2>

 <template v-for="name in names "::key="name">
  <h3 v-if="name === 'Azzam'">

{{ name }}
  </h3>
 </template><br>
 <h1>{{ 1 + 6 + 9 }}</h1>
 <h1>
  Adding function {{ add(15, -10 ,25) }}<br>
  Multipleier method - {{ multiplier() }}</h1> -->
  <h1>Event Handling:</h1>
  <h1>{{ name }}</h1>
  <div>
    <button v-on:mouseover="name = 'Ali'">click me </button>
  </div>
  <h1>{{ counter }}</h1>
  <div>
    <button v-on:click="counter += 1">Increment </button>
    <button v-on:click="counter -= 1">Decrement </button>
    short hand event listener:
    <button @click="increment">Increment by function</button>
    <button @click="decrement">Decrement by function </button>
  </div>
  <div ><pre>
    {{ JSON.stringify(formValues, null,2) }}
  </pre></div>
<form action="" method="post" @submit.prevent="submitForm">
  <div>
    <label for="name">Name:</label>
    <input type="text" id="name" v-model.trim.lazy="formValues.name "/>
  </div>
    <div>
    <label for="age">Age:</label>
    <input 
   @keyup.enter="submitForm" type="number" id="age" v-model.number="formValues.age "/>
  </div>
  <div>
    <label for="profile">Name:</label>
    <textarea type="text" id="profile" v-model="formValues.summaryProfile "/>
  </div>
  <div>
    <label for="country">Country:</label>
    <select type="text"  id="country" v-model="formValues.country ">
      <option value="SYR">Syria</option>
      <option value="UAE">United Emarites</option>
      <option value="KSA">Saudi Kindom</option>
      <option value="BLE">Belgium</option>
    </select>
  </div>
  <div>
    <label for="job-location">Job Location:</label>
    <select type="text" multiple id="job-location" v-model="formValues.jobLocation ">
      <option value="SYR">Syria</option>
      <option value="UAE">United Emarites</option>
      <option value="KSA">Saudi Kindom</option>
      <option value="BLE">Belgium</option>
    </select>
  </div>
  <div>
    <input type="checkbox"  id="remoteWork" v-model='formValues.remoteWork 'true-value="yes" false-value="no"/>
   <label for="remoteWork">Open to remote Work?</label>
  </div>
    <div>
      <label for="skillSet">skill set</label>
    <input type="checkbox"  id="html" value="html" v-model='formValues.skillSet '/>
    <label for="html" >html</label> 
       <input type="checkbox"  id="css" value="css"  v-model='formValues.skillSet '/>
    <label for="css" >css</label>
        <input type="checkbox"  id="js" value="js"  v-model='formValues.skillSet '/>
    <label  for="js" >js</label>
   
  </div>
  <div>
    <label for="yearsOfExperiense">years of Experiense</label>
        <input type="radio"  
        id="0-5" 
        value="0-5"
         v-model='formValues.yearsOfExperiense '/>
        <label for="0-5">0-5</label>
        <input type="radio"  id="5-15" value="5-15" v-model='formValues.yearsOfExperiense '/>
        <label for="5-15">5-15</label>
        <input type="radio"  id="15-20" value="15-20" v-model='formValues.yearsOfExperiense '/>
        <label for="15-20">15-20</label>                
  </div>
  <!--<div>
    <button>submit</button>
  </div>-->
</form>
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
      /*
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

      },*/
      num:"fdfd",
      display:true,
      showElement:true,
      
     names:['Azzam', 'Aziz', 'Ali'],
     baseMultiplier:5,
     name:"Azzam",
     counter:1,
     formValues:{
      name:'',
      summaryProfile:'',
      country:'',
      jobLocation:[],
      //remoteWork:false,
      remoteWork:'no',
      skillSet:[],
      yearsOfExperiense:'',
      age:null,
     },
    };
  }, methods: {
      add(a,b,c){
        return a + b -c ;
      },
      multiplier(){
      return 5 * this.baseMultiplier
     },
     increment(){
      this.counter += 1
     },
     decrement(){
      this.counter -= 1
     },
     submitForm(){
      //event.preventDefault();
      console.log(this.formValues)

     },
     },
     
}
</script>