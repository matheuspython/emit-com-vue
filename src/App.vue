<template>
  <h1>Site muito legal</h1>
  <AlertCard v-if="showAlert" @fecha="fecharAlert" text="seja bem vindo!!!" />
  <img class="imgGoku" v-if="!showAlert" src="https://static.wikia.nocookie.net/1e7ff1f7-6d62-4d43-9b48-e4bf98ff63f9" alt="gif goku se aquecendo">
</template>

<script>
import AlertCard from './components/AlertCard.vue';

export default {
  name: 'App',
  data() {
    return {
      showAlert: true
    }
  },
  methods:{
    fecharAlert(){
      this.showAlert = false
    }
  },
  components: {
    AlertCard
}
}
</script>

<style>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
h1{
  text-align: center;
  margin-top: 15px;
}

#app {
  font-family: sans-serif, Helvetica, Arial;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.imgGoku{
  width: 100%;
}
</style>
