<template>
    <div id="second">
    	<h2>second</h2>
    	<p>second组件接收值{{mg}}</p>
    </div>
</template>

<script>


export default {
  
  data () {
    return { 
      msg: 'world' 
    }
  },
  computed:{
     mg(){
        return this.$store.state.mg;
     }
  },
  mounted(){
  	  
  }
}
</script>


<style>
#second{  
	width: 300px;
	height: 120px;
	border: solid red 1px;
}
</style>