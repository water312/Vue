<template>
  <div>
    <h1>Hello world</h1>
    <div 
    class="static"
    v-bind:class="classObject">
    </div>
  </div>
</template>

<script>


export default {
  name: 'HelloWorld',
  // props: ['todo'],
  data() {
    return {
      isActive: true,
      hasError: null,
    }
  },
  computed: {
    classObject () {
      return {
        active: this.isActive && !this.error,
        'text-danger' : this.error && this.error.type === 'fatal',
      }
    }
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
