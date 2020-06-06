<template>
  <div>
      <h3>{{showNum}}</h3>
    <h4>当前最新值为：{{count}}</h4>
    <button @click="btnSubtraction1">-1</button>
    <button @click="btnSubtraction2">-N</button>
    <!-- <button @click="btnSubtraction3">-Async</button> -->
    <button @click="subAsync">-Async</button>
  </div>
</template>

<script>
import { mapState, mapMutations, mapActions,mapGetters } from "vuex";
export default {
  data() {
    return {};
  },
  computed: {
    ...mapState(["count"]),
    ...mapGetters(["showNum"])
  },
  methods: {
    ...mapMutations(["sub", "subN"]),
    ...mapActions(["subAsync"]),
    btnSubtraction1() {
      this.sub();
    },
    btnSubtraction2() {
      this.subN(5);
    },
    // btnSubtraction3() {
    //   this.subAsync();
    // }
  }
};
</script>

<style>
</style>