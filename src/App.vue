<template>
  <div id="app">
    <addition/>
    <p>-------------------------------------</p>
    <subtraction/>
  </div>
</template>

<script>
import addition from './components/addition'
import subtraction from './components/subtraction'
export default {
  name: 'App',
  components:{
    addition,
    subtraction
  }
}
</script>

<style>

</style>
