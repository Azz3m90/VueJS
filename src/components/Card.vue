<template>
 <div class="card">
  <div id="card-header">
   <slot name="header"></slot>
  </div>
    <div id="card-content">
   <slot ></slot>
  </div>
    <div id="card-footer">
   <slot name="footer"></slot>
  </div>
 </div>
</template>

<script>
export default {
 name:'Card',
 //props:['content'],
 setup () {
  

  return {}
 }
}
</script>

<style  scoped>
.card {
  width: 300px;
  border: 1px solid #ccc;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: 20px;
  background-color: #fff;
  margin: 20px auto;
  font-family: Arial, sans-serif;
}

.card h2 {
  font-size: 24px;
  margin-bottom: 10px;
  color: #333;
}

.card p {
  font-size: 16px;
  line-height: 1.6;
  color: #333;
}
</style>