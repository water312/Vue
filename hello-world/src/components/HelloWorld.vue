<template>
  <div class="hello">
    <!-- <h1>{{message}}</h1> -->
    <h3>이름: {{ firstName }}</h3>
    <h3>성: {{ lastName }}</h3>
    <h3>풀네임 : {{ fullName }}</h3>
    <button @click="fullNameGS = 'zerobase school'" >setter button</button>

  </div>
</template>

<script>


export default {
  name: 'HelloWorld',
  // props: ['todo'],
  data() {
    return {
      message: '안녕하세요! vue world',
      firstName: 'sungsu',
      lastName: 'CHO'
    }
  },
  computed: {
    fullName() {
      return this.firstName + ' ' + this.lastName
    },
    fullNameGS: {
      get: function () {
        return this.firstName + ' ' + this.lastName
      },
      set: function (e) {
        const names = e.split(' ')
        this.firstName = names[0]
        this.lastName = names[names.length - 1]
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
