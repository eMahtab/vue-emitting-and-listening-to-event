<template>
  <div id="child1" class="component">
    
    <h2>Child 1 Component</h2>
    <span>{{message}}</span><br/><br/>
    <button @click="change">Change</button>
  </div>
</template>

<script>
export default {
  props: ['message'],
  methods: {
    change(){  // Equivalent to change : function (){}
      this.message = "Changed";
      this.$emit('messageChanged',this.message);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#child1 {
  background-color: lightseagreen;
  
}
</style>
