<template>
  <v-app id="app">
    <top-bar @to-main-page="toMainPage" :sourceCodeLink="sourceCodeLink" :title="title"></top-bar>
    <router-view/>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      sourceCodeLink: 'https://github.com/ssthouse/visual-explain',
      title: 'Visual Explain'
    }
  },
  methods: {
    toMainPage() {
      this.$router.push('/')
    }
  },
  mounted() {
    window.$d3 = this.$d3
  }
}
</script>

<style>
body {
  width: 100vw;
  height: 100vh;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100vw;
  height: 100vh;
}
</style>
