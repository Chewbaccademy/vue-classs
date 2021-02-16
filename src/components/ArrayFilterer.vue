<template>
  <div id="main">
      <input type="number" name="" id="" v-model="id">
      <p> {{ texte }} </p>
      <ArrayOrder :id="id"></ArrayOrder>
  </div>
</template>

<script>
import { defineComponent } from 'vue'
import ArrayOrder from './ArrayOrder.vue';

export default defineComponent({
    name: 'ArrayFilterer',
    components: {
        ArrayOrder
    },
    data() {
        return {
            id: 0,
            texte: "À Talloires, au bord du lac d'Annecy, lors de ses dernières vacances de célibataire, Jérôme, un attaché culturel de 35 ans retrouve son amie Aurora qui écrit des romans sentimentaux, en s'inspirant entre autres des histoires réelles de Jérôme qu'à sa demande il lui raconte après les avoir vécues. Dans la maison vit une autre amie d'Aurora, Mme Walter, locataire pour l'été et mère de Laura, jeune fille à l'esprit vif d'une quinzaine d'années. La curiosité de Laura pour découvrir la vie va la conduire, à la suite de rencontres d'abord fortuites, puis qu'elle finit par provoquer avec Jérôme, à avoir une relation amicale tendre, cérébrale et presque amoureuse avec Jérôme. Apparaît ensuite Vincent, jeune homme du même âge que Laura, qui est son petit ami. Jérôme et Vincent se parlent posément et abondamment. Peu à peu, Laura se détache de Jérôme pour ne plus le voir à nouveau que fortuitement mais toujours amicalement, tandis que Jérôme se trouve fasciné par la fille de la propriétaire, Claire, plus âgée, d'environ 18 ans qui a pourtant une relation de couple avec Gilles, jeune homme un peu plus âgé et au physique séduisant. Jérôme n'aime pas Gilles et ressent un désir irrépressible de toucher le genou de Claire… Tout ce qui s'ensuit donnera à nouveau à Aurora de la matière pour écrire ses romans, mais sur une relation moins belle qu'entre Jérôme et Laura, et en dénouant ce qu'a vécu Jérôme et ce qu'il s'est imaginé de ce qu'elle s'aperçoit après son départ qui s'est réellement passé... "
        }
    },
})
</script>

<style>

</style>