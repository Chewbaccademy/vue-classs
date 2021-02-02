<template>
  <div id="listDiv">
    <h1 v-if="showText"> {{text}} </h1>
    <ul v-else id="list">
      <li v-for="item in items" v-bind:key="item"> {{item.id}} : {{item.nom}}</li>
    </ul>
    <button @click="toogleTextList">changer l'affichage</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'App',
  data() {
    return {
      text : "bienvenu sur l'appli",
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