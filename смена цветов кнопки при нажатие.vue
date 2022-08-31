<script> 
export default { 
  data() { 
    return { 
      color: ['red','white', 'blue','green'], 
      newColor: 'red'
    } 
  }, 
  methods: { 
    changeColor() { 
      let colorIndex = this.color.indexOf(this.newColor) 
      if (colorIndex !== this.color.length - 1) { 
        this.newColor = this.color[++colorIndex]
      } 
      else { 
        this.newColor = this.color[0]
      } 
    } 
  } 
} 
</script> 
 
<template> 
   <button :class="newColor" 
    v-on:click ="changeColor">Color: {{ count }}</button> 
</template> 
 
<style> 
   .white { 
       background-color: white; 
       width: 200px; 
       height: 200px;   
 
   } 
   .blue { 
       width: 200px; 
       height: 200px; 
       background-color: blue; 
 
   } 
  .red { 
       width: 200px; 
       height: 200px; 
       background-color: red; 
 
   } 
  .green { 
       background-color: green; 
       width: 200px; 
       height: 200px;   
 
   } 
</style>