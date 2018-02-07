<template>
    <div id="thirdchild">
    	<h2>donghua</h2>
    	<p>{{mg}}</p>
      <!-- <p>{{$store.state.mg}}</p> -->
      <button @click='action'>改变数值</button>
      <button @click='handleIncrement'>点击事件</button>
      {{flag}}
      <!-- <first></first> -->
      <!-- <second></second> -->
    </div>
</template>

<script>
// import store from '../assets/donghua'

// import first from './firstchild'
// import second from './second'

 
export default {
  components:{
    // first,
    // second
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      dat:''
    }
  },
  computed:{
    /* mg(){
        return this.$store.state.mg;
     },*/
     mg(){
        return this.$store.getters.mg;
     },
     flag(){
        return this.$store.state.flag;
     }
  },
  methods:{
    action(){
      //改变state中的值或者说将值存入state中,关注commit的两个参数
      this.$store.commit('increment',10);
       this.$router.push('/firstchild');
    },
    handleIncrement(){
       this.$store.commit('add',10);
    }
  },
  mounted(){
    
  }
}
</script>

<style type="text/css">
  #thirdchild{
    width: 400px;
    height: 300px;
    border:solid red 1px;
  }
</style>

