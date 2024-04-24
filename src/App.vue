

<template>
<h1>Full name: {{ firstName }} {{ lastName }}</h1>
<h1>computed Full name: {{ fullName }}</h1>
<button @click="changeFullName()">change name using setter and getter for computed values</button>
<button @click="items.push({id:4,title:'mouse',price:75})">Add items</button>
<h2>computed total : {{ total }}</h2>
<h2>method total : {{ getTotal() }}</h2>
<input type="text" v-model="country"/><br>
<template v-for="item in items":key="item.id">
  <h2 v-if="item.price > 100">{{ item.title }} {{ item.price }}</h2>
</template>
  <h2 v-for="item in expensiveItems">{{ item.title }} {{ item.price }}</h2>
</template>

<script>
export default {
  name:"App",
  data(){
    return {
      firstName:"Azzam",
      lastName:"Ali",
      items:[
        {
          id:1,
          title:"laptop",
          price:50,
        },
        {
          id:2,
          title:"headphone",
          price:150,
        },
        {
          id:3,
          title:"PC",
          price:250,
        },
      ],
      country:''
      
    }
  },
  methods:{
    getTotal(){
    console.log('getTotal Method called ')
          return this.items.reduce((total,curr) => (total = total + curr.price),0)
  },
  changeFullName(){
    this.fullName = "Azzam Aziz"
  }
},
  computed:{
    fullName:{
      get(){
        return `${this.firstName} ${this.lastName} `
      },
      set(value){
        const names = value.split(' ')
        this.firstName = names[0] 
        this.lastName = names[1] 
      }
    },
    total(){
       console.log('computed method is called')
      return this.items.reduce((total,curr) => (total = total + curr.price),0)
    },
    expensiveItems(){
      return this.items.filter(item =>item.price > 100)
    }
  },
}
</script>


<style scoped>

</style>