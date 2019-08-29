<template>
  <div class="second-nav-container">
    <div class="float-left">
      <div class="label-container display-flex">
        <div class="header-label">
          <strong>Property Analysis</strong>
        </div>
        <div class="property-name">{{property.name ? property.name : property.address}}</div>
      </div>
    </div>

    <div class="float-right cta-container">
      <button class="cta secondary" type="button">Share</button>
      <button class="cta primary" type="button">Export</button>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class SecondNavBar extends Vue {
  @Prop()
  private property!: object;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>