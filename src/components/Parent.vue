<script lang="ts">
import { Prop, Vue } from "vue-property-decorator";

export default abstract class Parent extends Vue {
  @Prop({ required: true }) readonly prop2!: string;
}
</script>
