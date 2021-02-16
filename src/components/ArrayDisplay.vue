<template>
  <div id="divList">
      <ul v-if="asc">
          <li v-for="obj in objects.sort(ascTri)" v-bind:key="obj">{{ obj.name }}</li>
      </ul>
      <ul v-else>
          <li v-for="obj in objects.sort(descTri)" v-bind:key="obj">{{ obj.name }}</li>
      </ul>
  </div>
</template>

<script>
import { defineComponent } from 'vue'
export default defineComponent({
    name: 'ArrayDisplay',
    props: {
        objects: Array,
        asc: Boolean
    },
    methods: {
        ascTri(obj1, obj2) {
            return obj1.name <= obj2.name ? -1 : 1;
        },
        descTri(obj1, obj2) {
            return obj1.name > obj2.name ? -1 : 1;
        }
    }
})
</script>

<style>

</style>