<template>
  <ArrayDisplay :asc="true" :objets="arrays[id]"></ArrayDisplay>
</template>

<script>
import { defineComponent } from 'vue'
import ArrayDisplay from './ArrayDisplay.vue';


export default defineComponent({
    name: 'ArrayOrder',
    components: {
        ArrayDisplay
    },
    props: {
        id: Number
    },
    data() {
        return {
            arrays: [
                [{id:1, name:"Boris"}, {id:2, name:"Basil"}, {id:3, name:"Victor"}],
                [{id:1, name:"Veronica"}, {id:2, name:"Selena"}, {id:3, name:"Sergent Garcia"}],
                [{id:1, name:"Jean-Luiz"}, {id:2, name:"Isabella"}, {id:3, name:"Saruman"}],
            ]
        }
    }

})
</script>

<style>

</style>