<script> 
export default { 
  data() { 
    return { 
      newColor: 'red'
    } 
  }, 
  methods: { 
    randomColor() {
    	var c = "#";
    	for (var i = 0; i < 6; i++) {
        c += (Math.random() * 16 | 0).toString(16);
    	} 
    	return c;
		},
    changeColor() { 
      this.newColor = this.randomColor()
    }
  } 
} 
</script> 
 
<template> 
   <button :class="newColor" v-bind:style=" `background-color: ${newColor}` " 
    v-on:click ="changeColor">Color: {{newColor}}</button> 
</template> 
 
<style> 
  
</style>