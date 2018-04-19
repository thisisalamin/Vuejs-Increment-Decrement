<template>
  <div>
    <v-progress-circular :size="100" :width="15" :rotate="360" :value="value" color="teal">
      {{ value }}
    </v-progress-circular>
    <v-spacer></v-spacer>
    <v-btn class="white--text" v-on:click="increment()" color="blue">Increment</v-btn>
    <v-btn class="white--text" v-on:click="decrement()" color="blue">Decrement</v-btn>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        value: 0
      }
    },
    methods : {
      increment : function () {
        if (this.value<=95) {       
          this.value = this.value+5;
        }
      },
      decrement : function () {
        if (this.value>0) {
          this.value = this.value-5;
        }
      }
    }
  }
</script>

<style lang="stylus" scoped>
  div
    text-align: center

  .progress-circular
    margin: 1rem
</style>
