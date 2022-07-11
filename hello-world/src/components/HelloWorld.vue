<template>
  <div>
    <h1>Hello world</h1>
    <div v-bind:style="{ color: activeColor, fontSize: fontSize + 'px' }" >
      첫번째 스타일 바인딩
    </div>
    <div v-bind:style="styleObject" >
      두번째 스타일 바인딩
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
      activeColor: 'red',
      fontSize: 30,
      styleObject: {
        color: 'red',
        fontSize: '13px',
      }
    }
  },
  computed: {
    
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
