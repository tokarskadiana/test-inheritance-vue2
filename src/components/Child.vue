<template>
  <p>Own property 'prop1': {{ prop1 }}, Inherited property 'prop2': {{ prop2 }}</p>
</template>
<script lang="ts">
import Parent from "./Parent.vue";
import {Component, Prop, Watch} from "vue-property-decorator";

@Component
export default class Child extends Parent {
  @Prop({ required: true }) readonly prop1!: string;
  @Watch("prop2")
  onInheritedPropChanged(newValue: string): void {
    console.log("prop2", newValue)
  }
}
</script>
