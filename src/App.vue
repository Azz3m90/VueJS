<template>
  <h4>Parent Component</h4>
  <ChildComponent />
</template>

<script>
import ChildComponent from '@/components/ChildComponent.vue'

export default {
  name: 'App',
  components: {
    ChildComponent,
  },
  data() {
    return {
      name: '',
    }
  },

  methods: {},
  computed: {},
  watch: {},
}
</script>

<style>
html,
body {
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

h1,
h2,
h3,
div,
p {
  display: block;
  margin: 10px 0; /* Adjust margin as needed */
}
h4 {
  color: olive;
}
</style>
