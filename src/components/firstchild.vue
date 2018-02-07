<template>
    <div id="firstchild">
    	<h2>firstchild</h2>
      <p>{{mssg}}</p>
      {{mg}}
      <button v-on:click='sendMsg'>firstchild组件传值</button>
    </div>
</template>

<script>
// import store from '../assets/donghua'

export default {
  
  data () {
    return {
      mssg:''
    }
  }, 
  computed:{
    mg(){
      return this.$store.state.mg;
    }
  },
  methods:{
  	sendMsg:function(){
      
  		this.$router.push('/second');
  	}
  },
  mounted(){
    
  }
}
</script>

<style type="text/css">
  #firstchild{ 
    width: 400px;
    height: 140px;
    border:solid #000000 1px;
  }
</style>

