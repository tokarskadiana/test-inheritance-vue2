<template>
  <div>
    <Child prop1="Child property" :prop2="prop2" />
    <input v-model="prop2">
  </div>
</template>

<script lang="ts">
import Child from "./components/Child.vue";
import {Component, Vue} from "vue-property-decorator";

@Component({
  components: {
    Child,
  },
})
export default class App extends Vue {
  prop2 = "Inherited property"
}
</script>
