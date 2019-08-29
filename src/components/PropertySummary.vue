<template>
  <div class="tile property-summary-container">
    <img
      class="property-image"
      src="https://maps.googleapis.com/maps/api/streetview?size=400x200&pitch=10&fov=180&location=320%20N%20Canal%20St,%20Chicago,%20IL%2060606&key=AIzaSyApsGVNO-Ms2sIJM4PtmwC5VfeutsZSExo"
    />
    <div class="tile-content">
      <div class="address-value text-left">320 N Canal St</div>
      <div class="city-value text-left">Chicago, IL 60606</div>
      <div class="units-value text-left">5 Units / Penthouse / 2015</div>
      <div class="avm-value text-left">7403292 AVM</div>
    </div>
    <div>
      <LateralNav :options="propertySections" />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
import LateralNav from "./LateralNav.vue";

@Component({
  components: {
    LateralNav
  }
})
export default class NavBar extends Vue {
  @Prop()
  private property!: object;

  private propertySections: object[] = [
    { name: "Comparables", selected: false },
    { name: "Operating Expenses", selected: true },
    { name: "Rent roll / Unit Mix", selected: false },
    { name: "Amenities", selected: false },
    { name: "Market", selected: false }
  ];
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>