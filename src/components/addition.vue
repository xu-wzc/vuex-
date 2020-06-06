<template>
<div>
  <h3>{{$store.getters.showNum}}</h3>
  <h4>当前最新值为：{{$store.state.count}}</h4>
<button @click="handle1">+1</button>
<button @click="handle2">+N</button>
<button @click="handle3">+async</button>
<button @click="handle4">+N+async </button>
</div>
</template>

<script>
export default {
data(){
  return{

  }
},
methods:{
  handle1(){
this.$store.commit('add')
  },
  handle2(){
this.$store.commit('addN',10)
  },
  handle3(){
this.$store.dispatch('addAsync')
  },
  handle4(){
this.$store.dispatch('addNAsync',8)
  }
}
}
</script>

<style>

</style>