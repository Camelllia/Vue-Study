<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <div>
      <h4>{{ name2 }} 원룸</h4>
      <P>{{ price2 }} 만원</P>
    </div>
    <div>
      <h4>{{ name1 }} 원룸</h4>
      <P>{{ price1 }} 만원</P>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      price1 : 60,
      price2 : 80,
      name1 : "MAC 환경",
      name2 : "테스트",
    }
  },
  components: {

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
