<template>
  <ArrayFilterer></ArrayFilterer>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import ArrayFilterer from './components/ArrayFilterer.vue';

export default defineComponent({
  name: 'App',
  components: {
    ArrayFilterer,
  },
  data() {
    return {
      text : "bienvenue sur l'appli",
      showText: true,
      items: [{id: 13, nom: "hervé"}, {id: 26, nom: "Pascal"}, {id: 32, nom: "Eglantine"}]
    }
  },
  methods: {
    toogleTextList() {
      this.showText = !this.showText;
    }
  }
})

</script>

<style>
#listDiv {
  position: absolute;
  top: 50vh;
  left: 50vw;
  transform: translate(-50%,-50%);
  display: flex;
  flex-direction: column;
  height: 100vh;
  width: 20vw;
  justify-content: space-around;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>